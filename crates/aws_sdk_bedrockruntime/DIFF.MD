# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/bedrockruntime`
- model: `aws-models/bedrock-runtime.json`
- package: `aws-sdk-bedrockruntime`
- library: `aws_sdk_bedrockruntime`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_get_async_invoke`: `GetAsyncInvoke`
- `op_list_async_invokes`: `ListAsyncInvokes`
- `op_start_async_invoke`: `StartAsyncInvoke`
- `op_apply_guardrail`: `ApplyGuardrail`
- `op_invoke_guardrail_checks`: `InvokeGuardrailChecks`
- `op_converse`: `Converse`
- `op_converse_stream`: `ConverseStream`
- `op_invoke_model`: `InvokeModel`
- `op_invoke_model_with_bidirectional_stream`: `InvokeModelWithBidirectionalStream`
- `op_invoke_model_with_response_stream`: `InvokeModelWithResponseStream`
- `op_count_tokens`: `CountTokens`

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
@@ -19,60 +19,47 @@
 version = "1"

 [dependencies.aws-credential-types]
-path = "../aws-credential-types"
 version = "1.3.0"

 [dependencies.aws-runtime]
-path = "../aws-runtime"
 features = ["event-stream"]
 version = "1.9.2"

 [dependencies.aws-sigv4]
-path = "../aws-sigv4"
 version = "1.5.1"

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
 features = ["client", "http-auth"]
 version = "1.14.0"

 [dependencies.aws-smithy-runtime-api]
-path = "../aws-smithy-runtime-api"
 features = ["client", "http-1x", "http-auth"]
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
@@ -97,50 +84,40 @@
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

@@ -171,3 +148,14 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_get_async_invoke = []
+op_list_async_invokes = []
+op_start_async_invoke = []
+op_apply_guardrail = []
+op_invoke_guardrail_checks = []
+op_converse = []
+op_converse_stream = []
+op_invoke_model = []
+op_invoke_model_with_bidirectional_stream = []
+op_invoke_model_with_response_stream = []
+op_count_tokens = []
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,12 +136,16 @@
     }
 }

+#[cfg(feature = "op_apply_guardrail")]
 mod apply_guardrail;

+#[cfg(feature = "op_converse")]
 mod converse;

+#[cfg(feature = "op_converse_stream")]
 mod converse_stream;

+#[cfg(feature = "op_count_tokens")]
 mod count_tokens;

 /// Operation customization and supporting types.
@@ -171,16 +175,23 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_get_async_invoke")]
 mod get_async_invoke;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod invoke_guardrail_checks;

+#[cfg(feature = "op_invoke_model")]
 mod invoke_model;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod invoke_model_with_bidirectional_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 mod invoke_model_with_response_stream;

+#[cfg(feature = "op_list_async_invokes")]
 mod list_async_invokes;

+#[cfg(feature = "op_start_async_invoke")]
 mod start_async_invoke;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,28 +3,135 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The request is denied because you do not have sufficient permissions to perform the requested action. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-access-denied">AccessDeniedException</a> in the Amazon Bedrock User Guide</p>
     AccessDeniedException(crate::types::error::AccessDeniedException),
+    #[cfg(feature = "op_start_async_invoke")]
     /// <p>Error occurred because of a conflict while performing an operation.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>An internal server error occurred. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-internal-failure">InternalFailure</a> in the Amazon Bedrock User Guide</p>
     InternalServerException(crate::types::error::InternalServerException),
+    #[cfg(any(
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>The request failed due to an error while processing the model.</p>
     ModelErrorException(crate::types::error::ModelErrorException),
+    #[cfg(any(
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>The model specified in the request is not ready to serve inference requests. The AWS SDK will automatically retry the operation up to 5 times. For information about configuring automatic retries, see <a href="https://docs.aws.amazon.com/sdkref/latest/guide/feature-retry-behavior.html">Retry behavior</a> in the <i>AWS SDKs and Tools</i> reference guide.</p>
     ModelNotReadyException(crate::types::error::ModelNotReadyException),
+    #[cfg(any(
+        feature = "op_converse_stream",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>An error occurred while streaming the response. Retry your request.</p>
     ModelStreamErrorException(crate::types::error::ModelStreamErrorException),
+    #[cfg(any(
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>The request took too long to process. Processing time exceeded the model timeout length.</p>
     ModelTimeoutException(crate::types::error::ModelTimeoutException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The specified resource ARN was not found. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-resource-not-found">ResourceNotFound</a> in the Amazon Bedrock User Guide</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>Your request exceeds the service quota for your account. You can view your quotas at <a href="https://docs.aws.amazon.com/servicequotas/latest/userguide/gs-request-quota.html">Viewing service quotas</a>. You can resubmit your request later.</p>
     ServiceQuotaExceededException(crate::types::error::ServiceQuotaExceededException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The service isn't currently available. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-service-unavailable">ServiceUnavailable</a> in the Amazon Bedrock User Guide</p>
     ServiceUnavailableException(crate::types::error::ServiceUnavailableException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>Your request was denied due to exceeding the account quotas for <i>Amazon Bedrock</i>. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-throttling-exception">ThrottlingException</a> in the Amazon Bedrock User Guide</p>
     ThrottlingException(crate::types::error::ThrottlingException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The input fails to satisfy the constraints specified by <i>Amazon Bedrock</i>. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-validation-error">ValidationError</a> in the Amazon Bedrock User Guide</p>
     ValidationException(crate::types::error::ValidationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -41,17 +148,124 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::AccessDeniedException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_async_invoke")]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::InternalServerException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelErrorException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelNotReadyException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelStreamErrorException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelTimeoutException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ThrottlingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ValidationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -76,22 +290,130 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::AccessDeniedException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_async_invoke")]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::InternalServerException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelErrorException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelNotReadyException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelStreamErrorException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelTimeoutException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceQuotaExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceUnavailableException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ThrottlingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ValidationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_apply_guardrail")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::apply_guardrail::ApplyGuardrailError, R>>
     for Error
@@ -113,6 +435,7 @@
         }
     }
 }
+#[cfg(feature = "op_apply_guardrail")]
 impl From<crate::operation::apply_guardrail::ApplyGuardrailError> for Error {
     fn from(err: crate::operation::apply_guardrail::ApplyGuardrailError) -> Self {
         match err {
@@ -141,6 +464,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::converse::ConverseError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -157,6 +481,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse")]
 impl From<crate::operation::converse::ConverseError> for Error {
     fn from(err: crate::operation::converse::ConverseError) -> Self {
         match err {
@@ -185,6 +510,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::converse_stream::ConverseStreamError, R>>
     for Error
@@ -206,6 +532,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl From<crate::operation::converse_stream::ConverseStreamError> for Error {
     fn from(err: crate::operation::converse_stream::ConverseStreamError) -> Self {
         match err {
@@ -243,6 +570,7 @@
         }
     }
 }
+#[cfg(feature = "op_count_tokens")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::count_tokens::CountTokensError, R>>
     for Error
 where
@@ -260,6 +588,7 @@
         }
     }
 }
+#[cfg(feature = "op_count_tokens")]
 impl From<crate::operation::count_tokens::CountTokensError> for Error {
     fn from(err: crate::operation::count_tokens::CountTokensError) -> Self {
         match err {
@@ -285,6 +614,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_async_invoke")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_async_invoke::GetAsyncInvokeError, R>>
     for Error
@@ -306,6 +636,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_async_invoke")]
 impl From<crate::operation::get_async_invoke::GetAsyncInvokeError> for Error {
     fn from(err: crate::operation::get_async_invoke::GetAsyncInvokeError) -> Self {
         match err {
@@ -325,6 +656,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_guardrail_checks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -350,6 +682,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_guardrail_checks")]
 impl From<crate::operation::invoke_guardrail_checks::InvokeGuardrailChecksError> for Error {
     fn from(err: crate::operation::invoke_guardrail_checks::InvokeGuardrailChecksError) -> Self {
         match err {
@@ -374,6 +707,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::invoke_model::InvokeModelError, R>>
     for Error
 where
@@ -391,6 +725,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model")]
 impl From<crate::operation::invoke_model::InvokeModelError> for Error {
     fn from(err: crate::operation::invoke_model::InvokeModelError) -> Self {
         match err {
@@ -428,6 +763,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -453,6 +789,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl From<crate::operation::invoke_model_with_bidirectional_stream::InvokeModelWithBidirectionalStreamError> for Error {
     fn from(
         err: crate::operation::invoke_model_with_bidirectional_stream::InvokeModelWithBidirectionalStreamError,
@@ -497,6 +834,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -522,6 +860,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl From<crate::operation::invoke_model_with_response_stream::InvokeModelWithResponseStreamError> for Error {
     fn from(err: crate::operation::invoke_model_with_response_stream::InvokeModelWithResponseStreamError) -> Self {
         match err {
@@ -562,6 +901,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_async_invokes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -587,6 +927,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_async_invokes")]
 impl From<crate::operation::list_async_invokes::ListAsyncInvokesError> for Error {
     fn from(err: crate::operation::list_async_invokes::ListAsyncInvokesError) -> Self {
         match err {
@@ -606,6 +947,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_async_invoke")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -631,6 +973,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_async_invoke")]
 impl From<crate::operation::start_async_invoke::StartAsyncInvokeError> for Error {
     fn from(err: crate::operation::start_async_invoke::StartAsyncInvokeError) -> Self {
         match err {
@@ -662,6 +1005,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::ConverseStreamOutputError, R>>
     for Error
 where
@@ -679,6 +1023,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl From<crate::types::error::ConverseStreamOutputError> for Error {
     fn from(err: crate::types::error::ConverseStreamOutputError) -> Self {
         match err {
@@ -701,6 +1046,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -726,6 +1072,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl From<crate::types::error::InvokeModelWithBidirectionalStreamInputError> for Error {
     fn from(err: crate::types::error::InvokeModelWithBidirectionalStreamInputError) -> Self {
         match err {
@@ -735,6 +1082,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -760,6 +1108,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl From<crate::types::error::InvokeModelWithBidirectionalStreamOutputError> for Error {
     fn from(err: crate::types::error::InvokeModelWithBidirectionalStreamOutputError) -> Self {
         match err {
@@ -787,6 +1136,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::ResponseStreamError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -803,6 +1153,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl From<crate::types::error::ResponseStreamError> for Error {
     fn from(err: crate::types::error::ResponseStreamError) -> Self {
         match err {
@@ -827,17 +1178,124 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::AccessDeniedException(inner) => inner.source(),
+            #[cfg(feature = "op_start_async_invoke")]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::InternalServerException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelErrorException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelNotReadyException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelStreamErrorException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelTimeoutException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ThrottlingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ValidationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -846,17 +1304,124 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::AccessDeniedException(e) => e.request_id(),
+            #[cfg(feature = "op_start_async_invoke")]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::InternalServerException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelErrorException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelNotReadyException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelStreamErrorException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelTimeoutException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceQuotaExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceUnavailableException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ThrottlingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
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
         InvokeModelWithBidirectionalStreamInputErrorMarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_eventstream::frame::MarshallMessage for InvokeModelWithBidirectionalStreamInputErrorMarshaller {
     type Input = crate::types::error::InvokeModelWithBidirectionalStreamInputError;
     fn marshall(
@@ -35,6 +36,7 @@
         InvokeModelWithBidirectionalStreamInputMarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_eventstream::frame::MarshallMessage for InvokeModelWithBidirectionalStreamInputMarshaller {
     type Input = crate::types::InvokeModelWithBidirectionalStreamInput;
     fn marshall(
@@ -75,6 +77,7 @@
         ConverseStreamOutputUnmarshaller
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for ConverseStreamOutputUnmarshaller {
     type Output = crate::types::ConverseStreamOutput;
     type Error = crate::types::error::ConverseStreamOutputError;
@@ -271,6 +274,7 @@
         InvokeModelWithBidirectionalStreamOutputUnmarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for InvokeModelWithBidirectionalStreamOutputUnmarshaller {
     type Output = crate::types::InvokeModelWithBidirectionalStreamOutput;
     type Error = crate::types::error::InvokeModelWithBidirectionalStreamOutputError;
@@ -430,6 +434,7 @@
         ResponseStreamUnmarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for ResponseStreamUnmarshaller {
     type Output = crate::types::ResponseStream;
     type Error = crate::types::error::ResponseStreamError;
```

### `src/lens.rs`

```diff
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) fn reflens_list_async_invokes_output_output_next_token(
     input: &crate::operation::list_async_invokes::ListAsyncInvokesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) fn lens_list_async_invokes_output_output_async_invoke_summaries(
     input: crate::operation::list_async_invokes::ListAsyncInvokesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AsyncInvokeSummary>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,35 +1,46 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_apply_guardrail")]
 /// Types for the `ApplyGuardrail` operation.
 pub mod apply_guardrail;

+#[cfg(feature = "op_converse")]
 /// Types for the `Converse` operation.
 pub mod converse;

+#[cfg(feature = "op_converse_stream")]
 /// Types for the `ConverseStream` operation.
 pub mod converse_stream;

+#[cfg(feature = "op_count_tokens")]
 /// Types for the `CountTokens` operation.
 pub mod count_tokens;

+#[cfg(feature = "op_get_async_invoke")]
 /// Types for the `GetAsyncInvoke` operation.
 pub mod get_async_invoke;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 /// Types for the `InvokeGuardrailChecks` operation.
 pub mod invoke_guardrail_checks;

+#[cfg(feature = "op_invoke_model")]
 /// Types for the `InvokeModel` operation.
 pub mod invoke_model;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 /// Types for the `InvokeModelWithBidirectionalStream` operation.
 pub mod invoke_model_with_bidirectional_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 /// Types for the `InvokeModelWithResponseStream` operation.
 pub mod invoke_model_with_response_stream;

+#[cfg(feature = "op_list_async_invokes")]
 /// Types for the `ListAsyncInvokes` operation.
 pub mod list_async_invokes;

+#[cfg(feature = "op_start_async_invoke")]
 /// Types for the `StartAsyncInvoke` operation.
 pub mod start_async_invoke;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,17 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +30,19 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,32 +54,58 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_apply_guardrail;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_count_tokens;

+#[cfg(feature = "op_get_async_invoke")]
 pub(crate) mod shape_get_async_invoke;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_invoke_guardrail_checks;

+#[cfg(feature = "op_invoke_model")]
 pub(crate) mod shape_invoke_model;

+#[cfg(feature = "op_invoke_model")]
 pub(crate) mod shape_invoke_model_input;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_invoke_model_with_bidirectional_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_invoke_model_with_response_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_invoke_model_with_response_stream_input;

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) mod shape_list_async_invokes;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_start_async_invoke;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -62,52 +114,175 @@
     }
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_access_denied_exception;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_apply_guardrail_input;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_input;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_input;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_output;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_count_tokens_input;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_internal_server_exception;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_invoke_guardrail_checks_input;

+#[cfg(feature = "op_invoke_model")]
 pub(crate) mod shape_invoke_model_output;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_invoke_model_with_bidirectional_stream_input;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_invoke_model_with_bidirectional_stream_output;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_invoke_model_with_response_stream_output;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_not_ready_exception;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_stream_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_timeout_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_service_unavailable_exception;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_start_async_invoke_input;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_throttling_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_validation_exception;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub fn parse_event_stream_error_metadata(
     payload: &::bytes::Bytes,
 ) -> ::std::result::Result<
@@ -117,380 +292,781 @@
     crate::json_errors::parse_error_metadata(payload, &::aws_smithy_runtime_api::http::Headers::new())
 }

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_async_invoke_output_data_config;

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) mod shape_async_invoke_summaries;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_bidirectional_input_payload_part;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_metrics;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_output;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_trace;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_assessment_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_message;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_results;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_usage_results;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_guardrail_configuration;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_content_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_coverage;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_output_content_list;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_guardrail_stream_configuration;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_inference_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_message;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_output_config;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_performance_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_prompt_variable_values;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_service_tier;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_system_content_block;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_tag;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_token_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_configuration;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_async_invoke_s3_output_data_config;

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) mod shape_async_invoke_summary;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_bidirectional_output_payload_part;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_cache_details_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_cache_point_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_content_block;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_delta_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_start_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_stop_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_metadata_event;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_converse_tokens_request;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_assessment;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_block;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_content_block;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_image_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_image_coverage;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_output_content;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_text_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_text_characters_coverage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_guardrail_trace_assessment;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_invoke_model_tokens_request;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_message_start_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_message_stop_event;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_output_format;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_payload_part;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_prompt_router_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_any_tool_choice;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_applied_guardrail_details;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_audio_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_auto_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_cache_detail;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citations_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_content_blocks;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_guardrail_assessment_list_map;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_guardrail_assessment_map;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_policy_assessment;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_result_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_result_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_entity_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_result_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_content_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_contextual_grounding_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_image_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_text_block;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_image_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_invocation_metrics;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_sensitive_information_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_topic_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_word_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_image_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_model_outputs;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_output_format_structure;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_reasoning_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_specific_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_system_tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_addition_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_removal_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_result_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_specification;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_use_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_video_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_audio_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_generated_content;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citations_config;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_start;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_metrics;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_error_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_finding_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_result_entry;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_content_filter_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_contextual_grounding_filters;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_image_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_custom_word_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_managed_word_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_origin_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_pii_entity_filter_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_regex_filter_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_topic_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_image_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_json_schema_definition;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_reasoning_text_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_input_schema;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_reference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_video_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_source_content;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_citations_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_content_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_content_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_contextual_grounding_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_custom_word;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_managed_word;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_pii_entity_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_regex_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_topic;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_image_block_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_image_block_start;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_reasoning_content_block_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_s3_location;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_result_block_start;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_result_blocks_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_use_block_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_use_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_generated_content_list;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_citation_source_content_list_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citations;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_char_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_chunk_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_page_location;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_impossible_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_invalid_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_no_translations_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_satisfiable_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_too_complex_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_ambiguous_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_valid_finding;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_content_blocks;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_location;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_result_block_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_result_content_blocks;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_web_location;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_citation_source_content_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_content_blocks;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_difference_scenario_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_logic_warning;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_rule_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_scenario;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_option_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_content_qualifier_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_source_content_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_input_text_reference_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_rule;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_statement_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_option;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_input_text_reference;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_statement;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_list;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) fn apply_guardrail_output_output_correct_errors(
     mut builder: crate::operation::apply_guardrail::builders::ApplyGuardrailOutputBuilder,
 ) -> crate::operation::apply_guardrail::builders::ApplyGuardrailOutputBuilder {
@@ -20,6 +21,7 @@
     builder
 }

+#[cfg(feature = "op_converse")]
 pub(crate) fn converse_output_output_correct_errors(
     mut builder: crate::operation::converse::builders::ConverseOutputBuilder,
 ) -> crate::operation::converse::builders::ConverseOutputBuilder {
@@ -44,6 +46,7 @@
     builder
 }

+#[cfg(feature = "op_count_tokens")]
 pub(crate) fn count_tokens_output_output_correct_errors(
     mut builder: crate::operation::count_tokens::builders::CountTokensOutputBuilder,
 ) -> crate::operation::count_tokens::builders::CountTokensOutputBuilder {
@@ -53,6 +56,7 @@
     builder
 }

+#[cfg(feature = "op_get_async_invoke")]
 pub(crate) fn get_async_invoke_output_output_correct_errors(
     mut builder: crate::operation::get_async_invoke::builders::GetAsyncInvokeOutputBuilder,
 ) -> crate::operation::get_async_invoke::builders::GetAsyncInvokeOutputBuilder {
@@ -74,6 +78,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn invoke_guardrail_checks_output_output_correct_errors(
     mut builder: crate::operation::invoke_guardrail_checks::builders::InvokeGuardrailChecksOutputBuilder,
 ) -> crate::operation::invoke_guardrail_checks::builders::InvokeGuardrailChecksOutputBuilder {
@@ -92,6 +97,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_model")]
 pub(crate) fn invoke_model_output_output_correct_errors(
     mut builder: crate::operation::invoke_model::builders::InvokeModelOutputBuilder,
 ) -> crate::operation::invoke_model::builders::InvokeModelOutputBuilder {
@@ -104,6 +110,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) fn invoke_model_with_response_stream_output_output_correct_errors(
     mut builder: crate::operation::invoke_model_with_response_stream::builders::InvokeModelWithResponseStreamOutputBuilder,
 ) -> crate::operation::invoke_model_with_response_stream::builders::InvokeModelWithResponseStreamOutputBuilder {
@@ -113,6 +120,7 @@
     builder
 }

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) fn start_async_invoke_output_output_correct_errors(
     mut builder: crate::operation::start_async_invoke::builders::StartAsyncInvokeOutputBuilder,
 ) -> crate::operation::start_async_invoke::builders::StartAsyncInvokeOutputBuilder {
@@ -122,6 +130,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailUsageBuilder,
 ) -> crate::types::builders::GuardrailUsageBuilder {
@@ -146,6 +159,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) fn token_usage_correct_errors(
     mut builder: crate::types::builders::TokenUsageBuilder,
 ) -> crate::types::builders::TokenUsageBuilder {
@@ -161,6 +175,7 @@
     builder
 }

+#[cfg(feature = "op_converse")]
 pub(crate) fn converse_metrics_correct_errors(
     mut builder: crate::types::builders::ConverseMetricsBuilder,
 ) -> crate::types::builders::ConverseMetricsBuilder {
@@ -170,6 +185,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) fn service_tier_correct_errors(
     mut builder: crate::types::builders::ServiceTierBuilder,
 ) -> crate::types::builders::ServiceTierBuilder {
@@ -179,6 +195,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) fn async_invoke_s3_output_data_config_correct_errors(
     mut builder: crate::types::builders::AsyncInvokeS3OutputDataConfigBuilder,
 ) -> crate::types::builders::AsyncInvokeS3OutputDataConfigBuilder {
@@ -188,6 +209,7 @@
     builder
 }

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) fn async_invoke_summary_correct_errors(
     mut builder: crate::types::builders::AsyncInvokeSummaryBuilder,
 ) -> crate::types::builders::AsyncInvokeSummaryBuilder {
@@ -206,6 +228,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_content_filter_result_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksContentFilterResultBuilder,
 ) -> crate::types::builders::GuardrailChecksContentFilterResultBuilder {
@@ -215,6 +238,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_content_filter_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksContentFilterUsageBuilder,
 ) -> crate::types::builders::GuardrailChecksContentFilterUsageBuilder {
@@ -224,6 +248,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_prompt_attack_result_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksPromptAttackResultBuilder,
 ) -> crate::types::builders::GuardrailChecksPromptAttackResultBuilder {
@@ -233,6 +258,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_prompt_attack_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksPromptAttackUsageBuilder,
 ) -> crate::types::builders::GuardrailChecksPromptAttackUsageBuilder {
@@ -242,6 +268,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_sensitive_information_result_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksSensitiveInformationResultBuilder,
 ) -> crate::types::builders::GuardrailChecksSensitiveInformationResultBuilder {
@@ -251,6 +278,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_sensitive_information_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksSensitiveInformationUsageBuilder,
 ) -> crate::types::builders::GuardrailChecksSensitiveInformationUsageBuilder {
@@ -260,6 +288,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn message_correct_errors(
     mut builder: crate::types::builders::MessageBuilder,
 ) -> crate::types::builders::MessageBuilder {
@@ -272,6 +301,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) fn cache_detail_correct_errors(
     mut builder: crate::types::builders::CacheDetailBuilder,
 ) -> crate::types::builders::CacheDetailBuilder {
@@ -284,6 +314,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn content_block_delta_event_correct_errors(
     mut builder: crate::types::builders::ContentBlockDeltaEventBuilder,
 ) -> crate::types::builders::ContentBlockDeltaEventBuilder {
@@ -296,6 +327,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn content_block_start_event_correct_errors(
     mut builder: crate::types::builders::ContentBlockStartEventBuilder,
 ) -> crate::types::builders::ContentBlockStartEventBuilder {
@@ -308,6 +340,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn content_block_stop_event_correct_errors(
     mut builder: crate::types::builders::ContentBlockStopEventBuilder,
 ) -> crate::types::builders::ContentBlockStopEventBuilder {
@@ -317,6 +350,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn converse_stream_metadata_event_correct_errors(
     mut builder: crate::types::builders::ConverseStreamMetadataEventBuilder,
 ) -> crate::types::builders::ConverseStreamMetadataEventBuilder {
@@ -337,6 +371,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_content_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailContentPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailContentPolicyAssessmentBuilder {
@@ -346,6 +385,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_sensitive_information_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailSensitiveInformationPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailSensitiveInformationPolicyAssessmentBuilder {
@@ -358,6 +402,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_topic_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailTopicPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailTopicPolicyAssessmentBuilder {
@@ -367,6 +416,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_word_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailWordPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailWordPolicyAssessmentBuilder {
@@ -379,6 +433,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn message_start_event_correct_errors(
     mut builder: crate::types::builders::MessageStartEventBuilder,
 ) -> crate::types::builders::MessageStartEventBuilder {
@@ -388,6 +443,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn message_stop_event_correct_errors(
     mut builder: crate::types::builders::MessageStopEventBuilder,
 ) -> crate::types::builders::MessageStopEventBuilder {
@@ -397,6 +453,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn converse_stream_metrics_correct_errors(
     mut builder: crate::types::builders::ConverseStreamMetricsBuilder,
 ) -> crate::types::builders::ConverseStreamMetricsBuilder {
@@ -406,6 +463,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_content_filter_result_entry_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksContentFilterResultEntryBuilder,
 ) -> crate::types::builders::GuardrailChecksContentFilterResultEntryBuilder {
@@ -420,6 +478,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_prompt_attack_result_entry_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksPromptAttackResultEntryBuilder,
 ) -> crate::types::builders::GuardrailChecksPromptAttackResultEntryBuilder {
@@ -434,6 +493,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_sensitive_information_result_entry_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksSensitiveInformationResultEntryBuilder,
 ) -> crate::types::builders::GuardrailChecksSensitiveInformationResultEntryBuilder {
@@ -460,6 +520,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn audio_block_correct_errors(
     mut builder: crate::types::builders::AudioBlockBuilder,
 ) -> crate::types::builders::AudioBlockBuilder {
@@ -472,6 +533,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn cache_point_block_correct_errors(
     mut builder: crate::types::builders::CachePointBlockBuilder,
 ) -> crate::types::builders::CachePointBlockBuilder {
@@ -481,6 +543,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn document_block_correct_errors(
     mut builder: crate::types::builders::DocumentBlockBuilder,
 ) -> crate::types::builders::DocumentBlockBuilder {
@@ -493,6 +556,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_content_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailContentFilterBuilder,
 ) -> crate::types::builders::GuardrailContentFilterBuilder {
@@ -514,6 +582,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_contextual_grounding_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailContextualGroundingFilterBuilder,
 ) -> crate::types::builders::GuardrailContextualGroundingFilterBuilder {
@@ -536,6 +609,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_custom_word_correct_errors(
     mut builder: crate::types::builders::GuardrailCustomWordBuilder,
 ) -> crate::types::builders::GuardrailCustomWordBuilder {
@@ -550,6 +628,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_managed_word_correct_errors(
     mut builder: crate::types::builders::GuardrailManagedWordBuilder,
 ) -> crate::types::builders::GuardrailManagedWordBuilder {
@@ -569,6 +652,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_pii_entity_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailPiiEntityFilterBuilder,
 ) -> crate::types::builders::GuardrailPiiEntityFilterBuilder {
@@ -586,6 +674,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_regex_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailRegexFilterBuilder,
 ) -> crate::types::builders::GuardrailRegexFilterBuilder {
@@ -597,6 +690,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_topic_correct_errors(
     mut builder: crate::types::builders::GuardrailTopicBuilder,
 ) -> crate::types::builders::GuardrailTopicBuilder {
@@ -614,6 +712,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn image_block_correct_errors(
     mut builder: crate::types::builders::ImageBlockBuilder,
 ) -> crate::types::builders::ImageBlockBuilder {
@@ -626,6 +725,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn image_block_start_correct_errors(
     mut builder: crate::types::builders::ImageBlockStartBuilder,
 ) -> crate::types::builders::ImageBlockStartBuilder {
@@ -635,6 +735,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn search_result_block_correct_errors(
     mut builder: crate::types::builders::SearchResultBlockBuilder,
 ) -> crate::types::builders::SearchResultBlockBuilder {
@@ -650,6 +751,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_addition_block_correct_errors(
     mut builder: crate::types::builders::ToolAdditionBlockBuilder,
 ) -> crate::types::builders::ToolAdditionBlockBuilder {
@@ -662,6 +764,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_removal_block_correct_errors(
     mut builder: crate::types::builders::ToolRemovalBlockBuilder,
 ) -> crate::types::builders::ToolRemovalBlockBuilder {
@@ -674,6 +777,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_result_block_correct_errors(
     mut builder: crate::types::builders::ToolResultBlockBuilder,
 ) -> crate::types::builders::ToolResultBlockBuilder {
@@ -686,6 +790,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn tool_result_block_start_correct_errors(
     mut builder: crate::types::builders::ToolResultBlockStartBuilder,
 ) -> crate::types::builders::ToolResultBlockStartBuilder {
@@ -695,6 +800,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_use_block_correct_errors(
     mut builder: crate::types::builders::ToolUseBlockBuilder,
 ) -> crate::types::builders::ToolUseBlockBuilder {
@@ -710,6 +816,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn tool_use_block_delta_correct_errors(
     mut builder: crate::types::builders::ToolUseBlockDeltaBuilder,
 ) -> crate::types::builders::ToolUseBlockDeltaBuilder {
@@ -719,6 +826,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn tool_use_block_start_correct_errors(
     mut builder: crate::types::builders::ToolUseBlockStartBuilder,
 ) -> crate::types::builders::ToolUseBlockStartBuilder {
@@ -731,6 +839,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn video_block_correct_errors(
     mut builder: crate::types::builders::VideoBlockBuilder,
 ) -> crate::types::builders::VideoBlockBuilder {
@@ -743,6 +852,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn citations_config_correct_errors(
     mut builder: crate::types::builders::CitationsConfigBuilder,
 ) -> crate::types::builders::CitationsConfigBuilder {
@@ -752,6 +862,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn guardrail_converse_image_block_correct_errors(
     mut builder: crate::types::builders::GuardrailConverseImageBlockBuilder,
 ) -> crate::types::builders::GuardrailConverseImageBlockBuilder {
@@ -766,6 +877,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn guardrail_converse_text_block_correct_errors(
     mut builder: crate::types::builders::GuardrailConverseTextBlockBuilder,
 ) -> crate::types::builders::GuardrailConverseTextBlockBuilder {
@@ -775,6 +887,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn reasoning_text_block_correct_errors(
     mut builder: crate::types::builders::ReasoningTextBlockBuilder,
 ) -> crate::types::builders::ReasoningTextBlockBuilder {
@@ -784,6 +897,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn s3_location_correct_errors(
     mut builder: crate::types::builders::S3LocationBuilder,
 ) -> crate::types::builders::S3LocationBuilder {
@@ -793,6 +907,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn search_result_content_block_correct_errors(
     mut builder: crate::types::builders::SearchResultContentBlockBuilder,
 ) -> crate::types::builders::SearchResultContentBlockBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,818 +1,1662 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_get_async_invoke", feature = "op_list_async_invokes"))]
 pub use crate::types::_async_invoke_status::AsyncInvokeStatus;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::_async_invoke_output_data_config::AsyncInvokeOutputDataConfig;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_sort_async_invocation_by::SortAsyncInvocationBy;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_sort_order::SortOrder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_content_source::GuardrailContentSource;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_output_scope::GuardrailOutputScope;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_usage::GuardrailUsage;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_action::GuardrailAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_coverage::GuardrailCoverage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_config::GuardrailChecksConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_results::GuardrailChecksResults;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_usage_results::GuardrailChecksUsageResults;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_inference_configuration::InferenceConfiguration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_configuration::ToolConfiguration;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_guardrail_configuration::GuardrailConfiguration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_performance_configuration::PerformanceConfiguration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_service_tier::ServiceTier;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_config::OutputConfig;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_output::ConverseOutput;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_stop_reason::StopReason;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_token_usage::TokenUsage;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_metrics::ConverseMetrics;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_trace::ConverseTrace;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_guardrail_stream_configuration::GuardrailStreamConfiguration;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_output::ConverseStreamOutput;

+#[cfg(any(feature = "op_invoke_model", feature = "op_invoke_model_with_response_stream"))]
 pub use crate::types::_trace::Trace;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::_performance_config_latency::PerformanceConfigLatency;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::_service_tier_type::ServiceTierType;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_invoke_model_with_bidirectional_stream_input::InvokeModelWithBidirectionalStreamInput;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_invoke_model_with_bidirectional_stream_output::InvokeModelWithBidirectionalStreamOutput;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub use crate::types::_response_stream::ResponseStream;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_count_tokens_input::CountTokensInput;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::_async_invoke_s3_output_data_config::AsyncInvokeS3OutputDataConfig;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_async_invoke_summary::AsyncInvokeSummary;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::_tag::Tag;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_content_block::GuardrailContentBlock;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_output_content::GuardrailOutputContent;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_assessment::GuardrailAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_text_characters_coverage::GuardrailTextCharactersCoverage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_image_coverage::GuardrailImageCoverage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_message::GuardrailChecksMessage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_config::GuardrailChecksContentFilterConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_config::GuardrailChecksPromptAttackConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_config::GuardrailChecksSensitiveInformationConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result::GuardrailChecksContentFilterResult;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result::GuardrailChecksPromptAttackResult;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result::GuardrailChecksSensitiveInformationResult;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_usage::GuardrailChecksContentFilterUsage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_usage::GuardrailChecksPromptAttackUsage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_usage::GuardrailChecksSensitiveInformationUsage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_message::Message;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_system_content_block::SystemContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_choice::ToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_guardrail_trace::GuardrailTrace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_prompt_variable_values::PromptVariableValues;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format::OutputFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_guardrail_trace_assessment::GuardrailTraceAssessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_prompt_router_trace::PromptRouterTrace;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_guardrail_stream_processing_mode::GuardrailStreamProcessingMode;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_start_event::MessageStartEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_start_event::ContentBlockStartEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_delta_event::ContentBlockDeltaEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_stop_event::ContentBlockStopEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_stop_event::MessageStopEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metadata_event::ConverseStreamMetadataEvent;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_input_payload_part::BidirectionalInputPayloadPart;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_output_payload_part::BidirectionalOutputPayloadPart;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub use crate::types::_payload_part::PayloadPart;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_invoke_model_tokens_request::InvokeModelTokensRequest;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_converse_tokens_request::ConverseTokensRequest;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_text_block::GuardrailTextBlock;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_block::GuardrailImageBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_policy_assessment::GuardrailTopicPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_policy_assessment::GuardrailContentPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_word_policy_assessment::GuardrailWordPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_sensitive_information_policy_assessment::GuardrailSensitiveInformationPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_policy_assessment::GuardrailContextualGroundingPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_policy_assessment::GuardrailAutomatedReasoningPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_invocation_metrics::GuardrailInvocationMetrics;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_applied_guardrail_details::AppliedGuardrailDetails;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_role::GuardrailChecksRole;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_conversation_role::ConversationRole;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_content_block::GuardrailConverseContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_point_block::CachePointBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool::Tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_auto_tool_choice::AutoToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_any_tool_choice::AnyToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_specific_tool_choice::SpecificToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format_type::OutputFormatType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format_structure::OutputFormatStructure;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_cache_detail::CacheDetail;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_start::ContentBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_delta::ContentBlockDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metrics::ConverseStreamMetrics;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_trace::ConverseStreamTrace;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_format::GuardrailImageFormat;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_source::GuardrailImageSource;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_ownership::GuardrailOwnership;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_block::GuardrailChecksContentBlock;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_category_config::GuardrailChecksContentFilterCategoryConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_category_config::GuardrailChecksPromptAttackCategoryConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_entity_config::GuardrailChecksSensitiveInformationEntityConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result_entry::GuardrailChecksContentFilterResultEntry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result_entry::GuardrailChecksPromptAttackResultEntry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result_entry::GuardrailChecksSensitiveInformationResultEntry;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_content_block::ContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_text_block::GuardrailConverseTextBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_block::GuardrailConverseImageBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_point_type::CachePointType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_ttl::CacheTtl;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_specification::ToolSpecification;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_system_tool::SystemTool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_json_schema_definition::JsonSchemaDefinition;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_start::ToolUseBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_result_block_start::ToolResultBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_start::ImageBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_delta::ToolUseBlockDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_reasoning_content_block_delta::ReasoningContentBlockDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citations_delta::CitationsDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_delta::ImageBlockDelta;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_content_qualifier::GuardrailContentQualifier;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic::GuardrailTopic;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter::GuardrailContentFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_custom_word::GuardrailCustomWord;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_managed_word::GuardrailManagedWord;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_pii_entity_filter::GuardrailPiiEntityFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_regex_filter::GuardrailRegexFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_filter::GuardrailContextualGroundingFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_finding::GuardrailAutomatedReasoningFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_origin::GuardrailOrigin;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_category::GuardrailChecksContentFilterCategory;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_category::GuardrailChecksPromptAttackCategory;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_entity_type::GuardrailChecksSensitiveInformationEntityType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_block::ImageBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_block::DocumentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_block::VideoBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_block::AudioBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_use_block::ToolUseBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_block::ToolResultBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_reasoning_content_block::ReasoningContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_content_block::CitationsContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_block::SearchResultBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_addition_block::ToolAdditionBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_removal_block::ToolRemovalBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_format::GuardrailConverseImageFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_source::GuardrailConverseImageSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_input_schema::ToolInputSchema;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_use_type::ToolUseType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_status::ToolResultStatus;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_format::ImageFormat;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_result_block_delta::ToolResultBlockDelta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation_location::CitationLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_source::ImageSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_error_block::ErrorBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_type::GuardrailTopicType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_policy_action::GuardrailTopicPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter_type::GuardrailContentFilterType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter_confidence::GuardrailContentFilterConfidence;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter_strength::GuardrailContentFilterStrength;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_policy_action::GuardrailContentPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_word_policy_action::GuardrailWordPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_managed_word_type::GuardrailManagedWordType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_pii_entity_type::GuardrailPiiEntityType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_sensitive_information_policy_action::GuardrailSensitiveInformationPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_filter_type::GuardrailContextualGroundingFilterType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_policy_action::GuardrailContextualGroundingPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_valid_finding::GuardrailAutomatedReasoningValidFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_invalid_finding::GuardrailAutomatedReasoningInvalidFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_satisfiable_finding::GuardrailAutomatedReasoningSatisfiableFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_impossible_finding::GuardrailAutomatedReasoningImpossibleFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_ambiguous_finding::GuardrailAutomatedReasoningTranslationAmbiguousFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_too_complex_finding::GuardrailAutomatedReasoningTooComplexFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_no_translations_finding::GuardrailAutomatedReasoningNoTranslationsFinding;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_format::DocumentFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_source::DocumentSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_config::CitationsConfig;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_format::VideoFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_source::VideoSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_format::AudioFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_source::AudioSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_reasoning_text_block::ReasoningTextBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_reference::ToolReference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_content_qualifier::GuardrailConverseContentQualifier;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citation_source_content_delta::CitationSourceContentDelta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_web_location::WebLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_char_location::DocumentCharLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_page_location::DocumentPageLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_chunk_location::DocumentChunkLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_location::SearchResultLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_s3_location::S3Location;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation::GuardrailAutomatedReasoningTranslation;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_scenario::GuardrailAutomatedReasoningScenario;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_logic_warning::GuardrailAutomatedReasoningLogicWarning;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_content_block::ToolResultContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation_generated_content::CitationGeneratedContent;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation::Citation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_content_block::SearchResultContentBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_rule::GuardrailAutomatedReasoningRule;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_logic_warning_type::GuardrailAutomatedReasoningLogicWarningType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_option::GuardrailAutomatedReasoningTranslationOption;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_content_block::DocumentContentBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_statement::GuardrailAutomatedReasoningStatement;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_input_text_reference::GuardrailAutomatedReasoningInputTextReference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation_source_content::CitationSourceContent;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _any_tool_choice;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _applied_guardrail_details;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _async_invoke_output_data_config;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _async_invoke_s3_output_data_config;

+#[cfg(any(feature = "op_get_async_invoke", feature = "op_list_async_invokes"))]
 mod _async_invoke_status;

+#[cfg(feature = "op_list_async_invokes")]
 mod _async_invoke_summary;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _audio_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _audio_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _audio_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _auto_tool_choice;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _bidirectional_input_payload_part;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _bidirectional_output_payload_part;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _cache_detail;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _cache_point_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _cache_point_type;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _cache_ttl;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation_generated_content;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation_source_content;

+#[cfg(feature = "op_converse_stream")]
 mod _citation_source_content_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citations_config;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citations_content_block;

+#[cfg(feature = "op_converse_stream")]
 mod _citations_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _content_block;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_delta_event;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_start;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_start_event;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_stop_event;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _conversation_role;

+#[cfg(feature = "op_converse")]
 mod _converse_metrics;

+#[cfg(feature = "op_converse")]
 mod _converse_output;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_metadata_event;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_metrics;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_output;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_trace;

+#[cfg(feature = "op_count_tokens")]
 mod _converse_tokens_request;

+#[cfg(feature = "op_converse")]
 mod _converse_trace;

+#[cfg(feature = "op_count_tokens")]
 mod _count_tokens_input;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_char_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_chunk_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_page_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _error_block;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_impossible_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_input_text_reference;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_invalid_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_logic_warning;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_logic_warning_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_no_translations_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_rule;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_satisfiable_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_scenario;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_statement;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_too_complex_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_translation;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_translation_ambiguous_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_translation_option;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_valid_finding;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_block;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_category;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_message;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_category;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_results;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_role;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_entity_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_entity_type;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_usage_results;

+#[cfg(feature = "op_converse")]
 mod _guardrail_configuration;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_content_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter_confidence;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter_strength;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_policy_assessment;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_content_qualifier;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_content_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_filter_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_content_qualifier;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_image_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_image_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_image_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_text_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_coverage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_custom_word;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_image_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_image_coverage;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_image_format;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_image_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_invocation_metrics;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_managed_word;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_managed_word_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_origin;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_output_content;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_output_scope;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_ownership;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_pii_entity_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_pii_entity_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_regex_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_sensitive_information_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_sensitive_information_policy_assessment;

+#[cfg(feature = "op_converse_stream")]
 mod _guardrail_stream_configuration;

+#[cfg(feature = "op_converse_stream")]
 mod _guardrail_stream_processing_mode;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_text_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_text_characters_coverage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic_type;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _guardrail_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _guardrail_trace_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_usage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_word_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_word_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _image_block;

+#[cfg(feature = "op_converse_stream")]
 mod _image_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _image_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _image_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _image_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _inference_configuration;

+#[cfg(feature = "op_count_tokens")]
 mod _invoke_model_tokens_request;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _invoke_model_with_bidirectional_stream_input;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _invoke_model_with_bidirectional_stream_output;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _json_schema_definition;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _message;

+#[cfg(feature = "op_converse_stream")]
 mod _message_start_event;

+#[cfg(feature = "op_converse_stream")]
 mod _message_stop_event;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_config;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_format_structure;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_format_type;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 mod _payload_part;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _performance_config_latency;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _performance_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _prompt_router_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _prompt_variable_values;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _reasoning_content_block;

+#[cfg(feature = "op_converse_stream")]
 mod _reasoning_content_block_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _reasoning_text_block;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 mod _response_stream;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _s3_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _search_result_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _search_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _search_result_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _service_tier;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _service_tier_type;

+#[cfg(feature = "op_list_async_invokes")]
 mod _sort_async_invocation_by;

+#[cfg(feature = "op_list_async_invokes")]
 mod _sort_order;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _specific_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _stop_reason;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _system_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _system_tool;

+#[cfg(feature = "op_start_async_invoke")]
 mod _tag;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _token_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_addition_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_input_schema;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_reference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_removal_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_result_block;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_result_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_result_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_result_status;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_specification;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_use_block;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_use_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_use_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_use_type;

+#[cfg(any(feature = "op_invoke_model", feature = "op_invoke_model_with_response_stream"))]
 mod _trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _video_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _video_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _video_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _web_location;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,250 +1,515 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_usage::GuardrailUsageBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_coverage::GuardrailCoverageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_config::GuardrailChecksConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_results::GuardrailChecksResultsBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_usage_results::GuardrailChecksUsageResultsBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_inference_configuration::InferenceConfigurationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_configuration::ToolConfigurationBuilder;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_guardrail_configuration::GuardrailConfigurationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_performance_configuration::PerformanceConfigurationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_service_tier::ServiceTierBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_config::OutputConfigBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_token_usage::TokenUsageBuilder;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_metrics::ConverseMetricsBuilder;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_trace::ConverseTraceBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_guardrail_stream_configuration::GuardrailStreamConfigurationBuilder;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::_async_invoke_s3_output_data_config::AsyncInvokeS3OutputDataConfigBuilder;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_async_invoke_summary::AsyncInvokeSummaryBuilder;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_output_content::GuardrailOutputContentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_assessment::GuardrailAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_text_characters_coverage::GuardrailTextCharactersCoverageBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_image_coverage::GuardrailImageCoverageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_message::GuardrailChecksMessageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_config::GuardrailChecksContentFilterConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_config::GuardrailChecksPromptAttackConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_config::GuardrailChecksSensitiveInformationConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result::GuardrailChecksContentFilterResultBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result::GuardrailChecksPromptAttackResultBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result::GuardrailChecksSensitiveInformationResultBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_usage::GuardrailChecksContentFilterUsageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_usage::GuardrailChecksPromptAttackUsageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_usage::GuardrailChecksSensitiveInformationUsageBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_message::MessageBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format::OutputFormatBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_guardrail_trace_assessment::GuardrailTraceAssessmentBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_prompt_router_trace::PromptRouterTraceBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_start_event::MessageStartEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_start_event::ContentBlockStartEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_delta_event::ContentBlockDeltaEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_stop_event::ContentBlockStopEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_stop_event::MessageStopEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metadata_event::ConverseStreamMetadataEventBuilder;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_input_payload_part::BidirectionalInputPayloadPartBuilder;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_output_payload_part::BidirectionalOutputPayloadPartBuilder;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub use crate::types::_payload_part::PayloadPartBuilder;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_invoke_model_tokens_request::InvokeModelTokensRequestBuilder;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_converse_tokens_request::ConverseTokensRequestBuilder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_text_block::GuardrailTextBlockBuilder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_block::GuardrailImageBlockBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_policy_assessment::GuardrailTopicPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_policy_assessment::GuardrailContentPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_word_policy_assessment::GuardrailWordPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_sensitive_information_policy_assessment::GuardrailSensitiveInformationPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_policy_assessment::GuardrailContextualGroundingPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_policy_assessment::GuardrailAutomatedReasoningPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_invocation_metrics::GuardrailInvocationMetricsBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_applied_guardrail_details::AppliedGuardrailDetailsBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_point_block::CachePointBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_auto_tool_choice::AutoToolChoiceBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_any_tool_choice::AnyToolChoiceBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_specific_tool_choice::SpecificToolChoiceBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_cache_detail::CacheDetailBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metrics::ConverseStreamMetricsBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_trace::ConverseStreamTraceBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_category_config::GuardrailChecksContentFilterCategoryConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_category_config::GuardrailChecksPromptAttackCategoryConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_entity_config::GuardrailChecksSensitiveInformationEntityConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result_entry::GuardrailChecksContentFilterResultEntryBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result_entry::GuardrailChecksPromptAttackResultEntryBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result_entry::GuardrailChecksSensitiveInformationResultEntryBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_text_block::GuardrailConverseTextBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_block::GuardrailConverseImageBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_specification::ToolSpecificationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_system_tool::SystemToolBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_json_schema_definition::JsonSchemaDefinitionBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_start::ToolUseBlockStartBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_result_block_start::ToolResultBlockStartBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_start::ImageBlockStartBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_delta::ToolUseBlockDeltaBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citations_delta::CitationsDeltaBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_delta::ImageBlockDeltaBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic::GuardrailTopicBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter::GuardrailContentFilterBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_custom_word::GuardrailCustomWordBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_managed_word::GuardrailManagedWordBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_pii_entity_filter::GuardrailPiiEntityFilterBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_regex_filter::GuardrailRegexFilterBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_filter::GuardrailContextualGroundingFilterBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_block::ImageBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_block::DocumentBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_block::VideoBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_block::AudioBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_use_block::ToolUseBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_block::ToolResultBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_content_block::CitationsContentBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_block::SearchResultBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_addition_block::ToolAdditionBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_removal_block::ToolRemovalBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_error_block::ErrorBlockBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_valid_finding::GuardrailAutomatedReasoningValidFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_invalid_finding::GuardrailAutomatedReasoningInvalidFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_satisfiable_finding::GuardrailAutomatedReasoningSatisfiableFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_impossible_finding::GuardrailAutomatedReasoningImpossibleFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_ambiguous_finding::GuardrailAutomatedReasoningTranslationAmbiguousFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_too_complex_finding::GuardrailAutomatedReasoningTooComplexFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_no_translations_finding::GuardrailAutomatedReasoningNoTranslationsFindingBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_config::CitationsConfigBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_reasoning_text_block::ReasoningTextBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_reference::ToolReferenceBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citation_source_content_delta::CitationSourceContentDeltaBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_web_location::WebLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_char_location::DocumentCharLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_page_location::DocumentPageLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_chunk_location::DocumentChunkLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_location::SearchResultLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_s3_location::S3LocationBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation::GuardrailAutomatedReasoningTranslationBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_scenario::GuardrailAutomatedReasoningScenarioBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_logic_warning::GuardrailAutomatedReasoningLogicWarningBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation::CitationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_content_block::SearchResultContentBlockBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_rule::GuardrailAutomatedReasoningRuleBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_option::GuardrailAutomatedReasoningTranslationOptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_statement::GuardrailAutomatedReasoningStatementBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_input_text_reference::GuardrailAutomatedReasoningInputTextReferenceBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,28 +1,136 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_validation_exception::ValidationException;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableException;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_error_exception::ModelErrorException;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_not_ready_exception::ModelNotReadyException;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_timeout_exception::ModelTimeoutException;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_stream_error_exception::ModelStreamErrorException;

+#[cfg(feature = "op_converse_stream")]
 /// Error type for the `ConverseStreamOutputError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -48,6 +156,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_converse_stream")]
 impl ConverseStreamOutputError {
     /// Creates the `ConverseStreamOutputError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -103,6 +212,7 @@
         matches!(self, Self::ServiceUnavailableException(_))
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::std::error::Error for ConverseStreamOutputError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -115,6 +225,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::std::fmt::Display for ConverseStreamOutputError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -135,6 +246,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for ConverseStreamOutputError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -143,6 +255,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for ConverseStreamOutputError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -165,6 +278,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for ConverseStreamOutputError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -176,6 +290,7 @@
         })
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::ConverseStreamOutputError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -182,6 +297,7 @@
     }
 }

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 /// Error type for the `InvokeModelWithBidirectionalStreamInputError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -197,6 +313,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl InvokeModelWithBidirectionalStreamInputError {
     /// Creates the `InvokeModelWithBidirectionalStreamInputError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -227,6 +344,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::error::Error for InvokeModelWithBidirectionalStreamInputError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -234,6 +352,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::fmt::Display for InvokeModelWithBidirectionalStreamInputError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -249,6 +368,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for InvokeModelWithBidirectionalStreamInputError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -257,6 +377,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for InvokeModelWithBidirectionalStreamInputError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -264,6 +385,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for InvokeModelWithBidirectionalStreamInputError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -275,6 +397,7 @@
         })
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::InvokeModelWithBidirectionalStreamInputError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -281,6 +404,7 @@
     }
 }

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 /// Error type for the `InvokeModelWithBidirectionalStreamOutputError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -308,6 +432,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl InvokeModelWithBidirectionalStreamOutputError {
     /// Creates the `InvokeModelWithBidirectionalStreamOutputError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -368,6 +493,7 @@
         matches!(self, Self::ServiceUnavailableException(_))
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::error::Error for InvokeModelWithBidirectionalStreamOutputError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -381,6 +507,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::fmt::Display for InvokeModelWithBidirectionalStreamOutputError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -402,6 +529,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for InvokeModelWithBidirectionalStreamOutputError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -410,6 +538,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for InvokeModelWithBidirectionalStreamOutputError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -435,6 +564,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for InvokeModelWithBidirectionalStreamOutputError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -446,6 +576,7 @@
         })
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::InvokeModelWithBidirectionalStreamOutputError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -452,6 +583,7 @@
     }
 }

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 /// Error type for the `ResponseStreamError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -479,6 +611,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ResponseStreamError {
     /// Creates the `ResponseStreamError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -539,6 +672,7 @@
         matches!(self, Self::ServiceUnavailableException(_))
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::std::error::Error for ResponseStreamError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -552,6 +686,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::std::fmt::Display for ResponseStreamError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -573,6 +708,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for ResponseStreamError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -581,6 +717,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for ResponseStreamError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -606,6 +743,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for ResponseStreamError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -617,6 +755,7 @@
         })
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::ResponseStreamError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -623,28 +762,135 @@
     }
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _access_denied_exception;

+#[cfg(feature = "op_start_async_invoke")]
 mod _conflict_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _internal_server_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_not_ready_exception;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_stream_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_timeout_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 mod _service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 mod _service_unavailable_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _throttling_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _validation_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,24 +1,131 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_validation_exception::ValidationExceptionBuilder;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_error_exception::ModelErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_not_ready_exception::ModelNotReadyExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_timeout_exception::ModelTimeoutExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_stream_error_exception::ModelStreamErrorExceptionBuilder;
```

## Unified diff

```diff
diff --git a/Cargo.toml b/Cargo.toml
--- a/Cargo.toml
+++ b/Cargo.toml
@@ -19,60 +19,47 @@
 version = "1"

 [dependencies.aws-credential-types]
-path = "../aws-credential-types"
 version = "1.3.0"

 [dependencies.aws-runtime]
-path = "../aws-runtime"
 features = ["event-stream"]
 version = "1.9.2"

 [dependencies.aws-sigv4]
-path = "../aws-sigv4"
 version = "1.5.1"

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
 features = ["client", "http-auth"]
 version = "1.14.0"

 [dependencies.aws-smithy-runtime-api]
-path = "../aws-smithy-runtime-api"
 features = ["client", "http-1x", "http-auth"]
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
@@ -97,50 +84,40 @@
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

@@ -171,3 +148,14 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_get_async_invoke = []
+op_list_async_invokes = []
+op_start_async_invoke = []
+op_apply_guardrail = []
+op_invoke_guardrail_checks = []
+op_converse = []
+op_converse_stream = []
+op_invoke_model = []
+op_invoke_model_with_bidirectional_stream = []
+op_invoke_model_with_response_stream = []
+op_count_tokens = []
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,12 +136,16 @@
     }
 }

+#[cfg(feature = "op_apply_guardrail")]
 mod apply_guardrail;

+#[cfg(feature = "op_converse")]
 mod converse;

+#[cfg(feature = "op_converse_stream")]
 mod converse_stream;

+#[cfg(feature = "op_count_tokens")]
 mod count_tokens;

 /// Operation customization and supporting types.
@@ -171,16 +175,23 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_get_async_invoke")]
 mod get_async_invoke;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod invoke_guardrail_checks;

+#[cfg(feature = "op_invoke_model")]
 mod invoke_model;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod invoke_model_with_bidirectional_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 mod invoke_model_with_response_stream;

+#[cfg(feature = "op_list_async_invokes")]
 mod list_async_invokes;

+#[cfg(feature = "op_start_async_invoke")]
 mod start_async_invoke;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,28 +3,135 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The request is denied because you do not have sufficient permissions to perform the requested action. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-access-denied">AccessDeniedException</a> in the Amazon Bedrock User Guide</p>
     AccessDeniedException(crate::types::error::AccessDeniedException),
+    #[cfg(feature = "op_start_async_invoke")]
     /// <p>Error occurred because of a conflict while performing an operation.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>An internal server error occurred. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-internal-failure">InternalFailure</a> in the Amazon Bedrock User Guide</p>
     InternalServerException(crate::types::error::InternalServerException),
+    #[cfg(any(
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>The request failed due to an error while processing the model.</p>
     ModelErrorException(crate::types::error::ModelErrorException),
+    #[cfg(any(
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>The model specified in the request is not ready to serve inference requests. The AWS SDK will automatically retry the operation up to 5 times. For information about configuring automatic retries, see <a href="https://docs.aws.amazon.com/sdkref/latest/guide/feature-retry-behavior.html">Retry behavior</a> in the <i>AWS SDKs and Tools</i> reference guide.</p>
     ModelNotReadyException(crate::types::error::ModelNotReadyException),
+    #[cfg(any(
+        feature = "op_converse_stream",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>An error occurred while streaming the response. Retry your request.</p>
     ModelStreamErrorException(crate::types::error::ModelStreamErrorException),
+    #[cfg(any(
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream"
+    ))]
     /// <p>The request took too long to process. Processing time exceeded the model timeout length.</p>
     ModelTimeoutException(crate::types::error::ModelTimeoutException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The specified resource ARN was not found. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-resource-not-found">ResourceNotFound</a> in the Amazon Bedrock User Guide</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>Your request exceeds the service quota for your account. You can view your quotas at <a href="https://docs.aws.amazon.com/servicequotas/latest/userguide/gs-request-quota.html">Viewing service quotas</a>. You can resubmit your request later.</p>
     ServiceQuotaExceededException(crate::types::error::ServiceQuotaExceededException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The service isn't currently available. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-service-unavailable">ServiceUnavailable</a> in the Amazon Bedrock User Guide</p>
     ServiceUnavailableException(crate::types::error::ServiceUnavailableException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>Your request was denied due to exceeding the account quotas for <i>Amazon Bedrock</i>. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-throttling-exception">ThrottlingException</a> in the Amazon Bedrock User Guide</p>
     ThrottlingException(crate::types::error::ThrottlingException),
+    #[cfg(any(
+        feature = "op_apply_guardrail",
+        feature = "op_converse",
+        feature = "op_converse_stream",
+        feature = "op_count_tokens",
+        feature = "op_get_async_invoke",
+        feature = "op_invoke_guardrail_checks",
+        feature = "op_invoke_model",
+        feature = "op_invoke_model_with_bidirectional_stream",
+        feature = "op_invoke_model_with_response_stream",
+        feature = "op_list_async_invokes",
+        feature = "op_start_async_invoke"
+    ))]
     /// <p>The input fails to satisfy the constraints specified by <i>Amazon Bedrock</i>. For troubleshooting this error, see <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/troubleshooting-api-error-codes.html#ts-validation-error">ValidationError</a> in the Amazon Bedrock User Guide</p>
     ValidationException(crate::types::error::ValidationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -41,17 +148,124 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::AccessDeniedException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_async_invoke")]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::InternalServerException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelErrorException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelNotReadyException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelStreamErrorException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelTimeoutException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ThrottlingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ValidationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -76,22 +290,130 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::AccessDeniedException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_async_invoke")]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::InternalServerException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelErrorException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelNotReadyException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelStreamErrorException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelTimeoutException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceQuotaExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceUnavailableException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ThrottlingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ValidationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_apply_guardrail")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::apply_guardrail::ApplyGuardrailError, R>>
     for Error
@@ -113,6 +435,7 @@
         }
     }
 }
+#[cfg(feature = "op_apply_guardrail")]
 impl From<crate::operation::apply_guardrail::ApplyGuardrailError> for Error {
     fn from(err: crate::operation::apply_guardrail::ApplyGuardrailError) -> Self {
         match err {
@@ -141,6 +464,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::converse::ConverseError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -157,6 +481,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse")]
 impl From<crate::operation::converse::ConverseError> for Error {
     fn from(err: crate::operation::converse::ConverseError) -> Self {
         match err {
@@ -185,6 +510,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::converse_stream::ConverseStreamError, R>>
     for Error
@@ -206,6 +532,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl From<crate::operation::converse_stream::ConverseStreamError> for Error {
     fn from(err: crate::operation::converse_stream::ConverseStreamError) -> Self {
         match err {
@@ -243,6 +570,7 @@
         }
     }
 }
+#[cfg(feature = "op_count_tokens")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::count_tokens::CountTokensError, R>>
     for Error
 where
@@ -260,6 +588,7 @@
         }
     }
 }
+#[cfg(feature = "op_count_tokens")]
 impl From<crate::operation::count_tokens::CountTokensError> for Error {
     fn from(err: crate::operation::count_tokens::CountTokensError) -> Self {
         match err {
@@ -285,6 +614,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_async_invoke")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_async_invoke::GetAsyncInvokeError, R>>
     for Error
@@ -306,6 +636,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_async_invoke")]
 impl From<crate::operation::get_async_invoke::GetAsyncInvokeError> for Error {
     fn from(err: crate::operation::get_async_invoke::GetAsyncInvokeError) -> Self {
         match err {
@@ -325,6 +656,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_guardrail_checks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -350,6 +682,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_guardrail_checks")]
 impl From<crate::operation::invoke_guardrail_checks::InvokeGuardrailChecksError> for Error {
     fn from(err: crate::operation::invoke_guardrail_checks::InvokeGuardrailChecksError) -> Self {
         match err {
@@ -374,6 +707,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::invoke_model::InvokeModelError, R>>
     for Error
 where
@@ -391,6 +725,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model")]
 impl From<crate::operation::invoke_model::InvokeModelError> for Error {
     fn from(err: crate::operation::invoke_model::InvokeModelError) -> Self {
         match err {
@@ -428,6 +763,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -453,6 +789,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl From<crate::operation::invoke_model_with_bidirectional_stream::InvokeModelWithBidirectionalStreamError> for Error {
     fn from(
         err: crate::operation::invoke_model_with_bidirectional_stream::InvokeModelWithBidirectionalStreamError,
@@ -497,6 +834,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -522,6 +860,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl From<crate::operation::invoke_model_with_response_stream::InvokeModelWithResponseStreamError> for Error {
     fn from(err: crate::operation::invoke_model_with_response_stream::InvokeModelWithResponseStreamError) -> Self {
         match err {
@@ -562,6 +901,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_async_invokes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -587,6 +927,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_async_invokes")]
 impl From<crate::operation::list_async_invokes::ListAsyncInvokesError> for Error {
     fn from(err: crate::operation::list_async_invokes::ListAsyncInvokesError) -> Self {
         match err {
@@ -606,6 +947,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_async_invoke")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -631,6 +973,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_async_invoke")]
 impl From<crate::operation::start_async_invoke::StartAsyncInvokeError> for Error {
     fn from(err: crate::operation::start_async_invoke::StartAsyncInvokeError) -> Self {
         match err {
@@ -662,6 +1005,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::ConverseStreamOutputError, R>>
     for Error
 where
@@ -679,6 +1023,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl From<crate::types::error::ConverseStreamOutputError> for Error {
     fn from(err: crate::types::error::ConverseStreamOutputError) -> Self {
         match err {
@@ -701,6 +1046,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -726,6 +1072,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl From<crate::types::error::InvokeModelWithBidirectionalStreamInputError> for Error {
     fn from(err: crate::types::error::InvokeModelWithBidirectionalStreamInputError) -> Self {
         match err {
@@ -735,6 +1082,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -760,6 +1108,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl From<crate::types::error::InvokeModelWithBidirectionalStreamOutputError> for Error {
     fn from(err: crate::types::error::InvokeModelWithBidirectionalStreamOutputError) -> Self {
         match err {
@@ -787,6 +1136,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::ResponseStreamError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -803,6 +1153,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl From<crate::types::error::ResponseStreamError> for Error {
     fn from(err: crate::types::error::ResponseStreamError) -> Self {
         match err {
@@ -827,17 +1178,124 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::AccessDeniedException(inner) => inner.source(),
+            #[cfg(feature = "op_start_async_invoke")]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::InternalServerException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelErrorException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelNotReadyException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelStreamErrorException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Error::ModelTimeoutException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ThrottlingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Error::ValidationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -846,17 +1304,124 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::AccessDeniedException(e) => e.request_id(),
+            #[cfg(feature = "op_start_async_invoke")]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::InternalServerException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelErrorException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelNotReadyException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse_stream",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelStreamErrorException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream"
+            ))]
             Self::ModelTimeoutException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceQuotaExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ServiceUnavailableException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ThrottlingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_apply_guardrail",
+                feature = "op_converse",
+                feature = "op_converse_stream",
+                feature = "op_count_tokens",
+                feature = "op_get_async_invoke",
+                feature = "op_invoke_guardrail_checks",
+                feature = "op_invoke_model",
+                feature = "op_invoke_model_with_bidirectional_stream",
+                feature = "op_invoke_model_with_response_stream",
+                feature = "op_list_async_invokes",
+                feature = "op_start_async_invoke"
+            ))]
             Self::ValidationException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/event_stream_serde.rs b/src/event_stream_serde.rs
--- a/src/event_stream_serde.rs
+++ b/src/event_stream_serde.rs
@@ -8,6 +8,7 @@
         InvokeModelWithBidirectionalStreamInputErrorMarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_eventstream::frame::MarshallMessage for InvokeModelWithBidirectionalStreamInputErrorMarshaller {
     type Input = crate::types::error::InvokeModelWithBidirectionalStreamInputError;
     fn marshall(
@@ -35,6 +36,7 @@
         InvokeModelWithBidirectionalStreamInputMarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_eventstream::frame::MarshallMessage for InvokeModelWithBidirectionalStreamInputMarshaller {
     type Input = crate::types::InvokeModelWithBidirectionalStreamInput;
     fn marshall(
@@ -75,6 +77,7 @@
         ConverseStreamOutputUnmarshaller
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for ConverseStreamOutputUnmarshaller {
     type Output = crate::types::ConverseStreamOutput;
     type Error = crate::types::error::ConverseStreamOutputError;
@@ -271,6 +274,7 @@
         InvokeModelWithBidirectionalStreamOutputUnmarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for InvokeModelWithBidirectionalStreamOutputUnmarshaller {
     type Output = crate::types::InvokeModelWithBidirectionalStreamOutput;
     type Error = crate::types::error::InvokeModelWithBidirectionalStreamOutputError;
@@ -430,6 +434,7 @@
         ResponseStreamUnmarshaller
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for ResponseStreamUnmarshaller {
     type Output = crate::types::ResponseStream;
     type Error = crate::types::error::ResponseStreamError;
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) fn reflens_list_async_invokes_output_output_next_token(
     input: &crate::operation::list_async_invokes::ListAsyncInvokesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) fn lens_list_async_invokes_output_output_async_invoke_summaries(
     input: crate::operation::list_async_invokes::ListAsyncInvokesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AsyncInvokeSummary>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,35 +1,46 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_apply_guardrail")]
 /// Types for the `ApplyGuardrail` operation.
 pub mod apply_guardrail;

+#[cfg(feature = "op_converse")]
 /// Types for the `Converse` operation.
 pub mod converse;

+#[cfg(feature = "op_converse_stream")]
 /// Types for the `ConverseStream` operation.
 pub mod converse_stream;

+#[cfg(feature = "op_count_tokens")]
 /// Types for the `CountTokens` operation.
 pub mod count_tokens;

+#[cfg(feature = "op_get_async_invoke")]
 /// Types for the `GetAsyncInvoke` operation.
 pub mod get_async_invoke;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 /// Types for the `InvokeGuardrailChecks` operation.
 pub mod invoke_guardrail_checks;

+#[cfg(feature = "op_invoke_model")]
 /// Types for the `InvokeModel` operation.
 pub mod invoke_model;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 /// Types for the `InvokeModelWithBidirectionalStream` operation.
 pub mod invoke_model_with_bidirectional_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 /// Types for the `InvokeModelWithResponseStream` operation.
 pub mod invoke_model_with_response_stream;

+#[cfg(feature = "op_list_async_invokes")]
 /// Types for the `ListAsyncInvokes` operation.
 pub mod list_async_invokes;

+#[cfg(feature = "op_start_async_invoke")]
 /// Types for the `StartAsyncInvoke` operation.
 pub mod start_async_invoke;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,17 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +30,19 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,32 +54,58 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_apply_guardrail;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_count_tokens;

+#[cfg(feature = "op_get_async_invoke")]
 pub(crate) mod shape_get_async_invoke;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_invoke_guardrail_checks;

+#[cfg(feature = "op_invoke_model")]
 pub(crate) mod shape_invoke_model;

+#[cfg(feature = "op_invoke_model")]
 pub(crate) mod shape_invoke_model_input;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_invoke_model_with_bidirectional_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_invoke_model_with_response_stream;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_invoke_model_with_response_stream_input;

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) mod shape_list_async_invokes;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_start_async_invoke;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -62,52 +114,175 @@
     }
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_access_denied_exception;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_apply_guardrail_input;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_input;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_input;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_output;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_count_tokens_input;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_internal_server_exception;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_invoke_guardrail_checks_input;

+#[cfg(feature = "op_invoke_model")]
 pub(crate) mod shape_invoke_model_output;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_invoke_model_with_bidirectional_stream_input;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_invoke_model_with_bidirectional_stream_output;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_invoke_model_with_response_stream_output;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_not_ready_exception;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_stream_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub(crate) mod shape_model_timeout_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_service_unavailable_exception;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_start_async_invoke_input;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_throttling_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_validation_exception;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub fn parse_event_stream_error_metadata(
     payload: &::bytes::Bytes,
 ) -> ::std::result::Result<
@@ -117,380 +292,781 @@
     crate::json_errors::parse_error_metadata(payload, &::aws_smithy_runtime_api::http::Headers::new())
 }

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_async_invoke_output_data_config;

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) mod shape_async_invoke_summaries;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_bidirectional_input_payload_part;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_metrics;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_output;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_converse_trace;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_assessment_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_message;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_results;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_usage_results;

+#[cfg(feature = "op_converse")]
 pub(crate) mod shape_guardrail_configuration;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_content_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_coverage;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_output_content_list;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_guardrail_stream_configuration;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_inference_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_message;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_output_config;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_performance_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_prompt_variable_values;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_service_tier;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_system_content_block;

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) mod shape_tag;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_token_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_configuration;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) mod shape_async_invoke_s3_output_data_config;

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) mod shape_async_invoke_summary;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub(crate) mod shape_bidirectional_output_payload_part;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_cache_details_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_cache_point_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_content_block;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_delta_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_start_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_stop_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_metadata_event;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_converse_tokens_request;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_assessment;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_block;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_content_block;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_image_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_image_coverage;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_output_content;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_text_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_text_characters_coverage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_guardrail_trace_assessment;

+#[cfg(feature = "op_count_tokens")]
 pub(crate) mod shape_invoke_model_tokens_request;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_message_start_event;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_message_stop_event;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_output_format;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) mod shape_payload_part;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_prompt_router_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_any_tool_choice;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_applied_guardrail_details;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_audio_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_auto_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_cache_detail;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citations_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_content_blocks;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_guardrail_assessment_list_map;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_guardrail_assessment_map;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_policy_assessment;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_result_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_result_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_entity_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_result_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_content_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_contextual_grounding_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_image_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_text_block;

+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) mod shape_guardrail_image_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_invocation_metrics;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_sensitive_information_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_topic_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_word_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_image_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_model_outputs;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_output_format_structure;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_reasoning_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_specific_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_system_tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_addition_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_removal_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_result_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_specification;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_use_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_video_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_audio_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_generated_content;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citations_config;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_content_block_start;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_metrics;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_converse_stream_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_error_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_finding_list;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_content_filter_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_prompt_attack_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) mod shape_guardrail_checks_sensitive_information_result_entry;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_content_filter_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_contextual_grounding_filters;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_image_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_custom_word_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_managed_word_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_origin_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_pii_entity_filter_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_regex_filter_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_topic_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_image_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) mod shape_json_schema_definition;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_reasoning_text_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_input_schema;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_reference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_video_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_source_content;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_citations_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_content_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_content_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_contextual_grounding_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_custom_word;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_managed_word;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_pii_entity_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_regex_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_topic;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_image_block_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_image_block_start;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_reasoning_content_block_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_s3_location;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_result_block_start;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_result_blocks_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_use_block_delta;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_use_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_generated_content_list;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_citation_source_content_list_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citations;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_char_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_chunk_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_page_location;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_impossible_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_invalid_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_no_translations_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_satisfiable_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_too_complex_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_ambiguous_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_valid_finding;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_content_blocks;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_search_result_location;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_tool_result_block_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_tool_result_content_blocks;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_web_location;

+#[cfg(feature = "op_converse_stream")]
 pub(crate) mod shape_citation_source_content_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_document_content_blocks;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_difference_scenario_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_logic_warning;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_rule_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_scenario;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_option_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_guardrail_converse_content_qualifier_list;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) mod shape_citation_source_content_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_input_text_reference_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_rule;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_statement_list;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_option;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_input_text_reference;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_statement;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) mod shape_guardrail_automated_reasoning_translation_list;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_apply_guardrail")]
 pub(crate) fn apply_guardrail_output_output_correct_errors(
     mut builder: crate::operation::apply_guardrail::builders::ApplyGuardrailOutputBuilder,
 ) -> crate::operation::apply_guardrail::builders::ApplyGuardrailOutputBuilder {
@@ -20,6 +21,7 @@
     builder
 }

+#[cfg(feature = "op_converse")]
 pub(crate) fn converse_output_output_correct_errors(
     mut builder: crate::operation::converse::builders::ConverseOutputBuilder,
 ) -> crate::operation::converse::builders::ConverseOutputBuilder {
@@ -44,6 +46,7 @@
     builder
 }

+#[cfg(feature = "op_count_tokens")]
 pub(crate) fn count_tokens_output_output_correct_errors(
     mut builder: crate::operation::count_tokens::builders::CountTokensOutputBuilder,
 ) -> crate::operation::count_tokens::builders::CountTokensOutputBuilder {
@@ -53,6 +56,7 @@
     builder
 }

+#[cfg(feature = "op_get_async_invoke")]
 pub(crate) fn get_async_invoke_output_output_correct_errors(
     mut builder: crate::operation::get_async_invoke::builders::GetAsyncInvokeOutputBuilder,
 ) -> crate::operation::get_async_invoke::builders::GetAsyncInvokeOutputBuilder {
@@ -74,6 +78,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn invoke_guardrail_checks_output_output_correct_errors(
     mut builder: crate::operation::invoke_guardrail_checks::builders::InvokeGuardrailChecksOutputBuilder,
 ) -> crate::operation::invoke_guardrail_checks::builders::InvokeGuardrailChecksOutputBuilder {
@@ -92,6 +97,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_model")]
 pub(crate) fn invoke_model_output_output_correct_errors(
     mut builder: crate::operation::invoke_model::builders::InvokeModelOutputBuilder,
 ) -> crate::operation::invoke_model::builders::InvokeModelOutputBuilder {
@@ -104,6 +110,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub(crate) fn invoke_model_with_response_stream_output_output_correct_errors(
     mut builder: crate::operation::invoke_model_with_response_stream::builders::InvokeModelWithResponseStreamOutputBuilder,
 ) -> crate::operation::invoke_model_with_response_stream::builders::InvokeModelWithResponseStreamOutputBuilder {
@@ -113,6 +120,7 @@
     builder
 }

+#[cfg(feature = "op_start_async_invoke")]
 pub(crate) fn start_async_invoke_output_output_correct_errors(
     mut builder: crate::operation::start_async_invoke::builders::StartAsyncInvokeOutputBuilder,
 ) -> crate::operation::start_async_invoke::builders::StartAsyncInvokeOutputBuilder {
@@ -122,6 +130,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailUsageBuilder,
 ) -> crate::types::builders::GuardrailUsageBuilder {
@@ -146,6 +159,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) fn token_usage_correct_errors(
     mut builder: crate::types::builders::TokenUsageBuilder,
 ) -> crate::types::builders::TokenUsageBuilder {
@@ -161,6 +175,7 @@
     builder
 }

+#[cfg(feature = "op_converse")]
 pub(crate) fn converse_metrics_correct_errors(
     mut builder: crate::types::builders::ConverseMetricsBuilder,
 ) -> crate::types::builders::ConverseMetricsBuilder {
@@ -170,6 +185,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) fn service_tier_correct_errors(
     mut builder: crate::types::builders::ServiceTierBuilder,
 ) -> crate::types::builders::ServiceTierBuilder {
@@ -179,6 +195,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub(crate) fn async_invoke_s3_output_data_config_correct_errors(
     mut builder: crate::types::builders::AsyncInvokeS3OutputDataConfigBuilder,
 ) -> crate::types::builders::AsyncInvokeS3OutputDataConfigBuilder {
@@ -188,6 +209,7 @@
     builder
 }

+#[cfg(feature = "op_list_async_invokes")]
 pub(crate) fn async_invoke_summary_correct_errors(
     mut builder: crate::types::builders::AsyncInvokeSummaryBuilder,
 ) -> crate::types::builders::AsyncInvokeSummaryBuilder {
@@ -206,6 +228,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_content_filter_result_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksContentFilterResultBuilder,
 ) -> crate::types::builders::GuardrailChecksContentFilterResultBuilder {
@@ -215,6 +238,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_content_filter_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksContentFilterUsageBuilder,
 ) -> crate::types::builders::GuardrailChecksContentFilterUsageBuilder {
@@ -224,6 +248,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_prompt_attack_result_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksPromptAttackResultBuilder,
 ) -> crate::types::builders::GuardrailChecksPromptAttackResultBuilder {
@@ -233,6 +258,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_prompt_attack_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksPromptAttackUsageBuilder,
 ) -> crate::types::builders::GuardrailChecksPromptAttackUsageBuilder {
@@ -242,6 +268,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_sensitive_information_result_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksSensitiveInformationResultBuilder,
 ) -> crate::types::builders::GuardrailChecksSensitiveInformationResultBuilder {
@@ -251,6 +278,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_sensitive_information_usage_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksSensitiveInformationUsageBuilder,
 ) -> crate::types::builders::GuardrailChecksSensitiveInformationUsageBuilder {
@@ -260,6 +288,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn message_correct_errors(
     mut builder: crate::types::builders::MessageBuilder,
 ) -> crate::types::builders::MessageBuilder {
@@ -272,6 +301,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub(crate) fn cache_detail_correct_errors(
     mut builder: crate::types::builders::CacheDetailBuilder,
 ) -> crate::types::builders::CacheDetailBuilder {
@@ -284,6 +314,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn content_block_delta_event_correct_errors(
     mut builder: crate::types::builders::ContentBlockDeltaEventBuilder,
 ) -> crate::types::builders::ContentBlockDeltaEventBuilder {
@@ -296,6 +327,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn content_block_start_event_correct_errors(
     mut builder: crate::types::builders::ContentBlockStartEventBuilder,
 ) -> crate::types::builders::ContentBlockStartEventBuilder {
@@ -308,6 +340,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn content_block_stop_event_correct_errors(
     mut builder: crate::types::builders::ContentBlockStopEventBuilder,
 ) -> crate::types::builders::ContentBlockStopEventBuilder {
@@ -317,6 +350,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn converse_stream_metadata_event_correct_errors(
     mut builder: crate::types::builders::ConverseStreamMetadataEventBuilder,
 ) -> crate::types::builders::ConverseStreamMetadataEventBuilder {
@@ -337,6 +371,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_content_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailContentPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailContentPolicyAssessmentBuilder {
@@ -346,6 +385,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_sensitive_information_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailSensitiveInformationPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailSensitiveInformationPolicyAssessmentBuilder {
@@ -358,6 +402,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_topic_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailTopicPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailTopicPolicyAssessmentBuilder {
@@ -367,6 +416,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_word_policy_assessment_correct_errors(
     mut builder: crate::types::builders::GuardrailWordPolicyAssessmentBuilder,
 ) -> crate::types::builders::GuardrailWordPolicyAssessmentBuilder {
@@ -379,6 +433,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn message_start_event_correct_errors(
     mut builder: crate::types::builders::MessageStartEventBuilder,
 ) -> crate::types::builders::MessageStartEventBuilder {
@@ -388,6 +443,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn message_stop_event_correct_errors(
     mut builder: crate::types::builders::MessageStopEventBuilder,
 ) -> crate::types::builders::MessageStopEventBuilder {
@@ -397,6 +453,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn converse_stream_metrics_correct_errors(
     mut builder: crate::types::builders::ConverseStreamMetricsBuilder,
 ) -> crate::types::builders::ConverseStreamMetricsBuilder {
@@ -406,6 +463,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_content_filter_result_entry_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksContentFilterResultEntryBuilder,
 ) -> crate::types::builders::GuardrailChecksContentFilterResultEntryBuilder {
@@ -420,6 +478,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_prompt_attack_result_entry_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksPromptAttackResultEntryBuilder,
 ) -> crate::types::builders::GuardrailChecksPromptAttackResultEntryBuilder {
@@ -434,6 +493,7 @@
     builder
 }

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub(crate) fn guardrail_checks_sensitive_information_result_entry_correct_errors(
     mut builder: crate::types::builders::GuardrailChecksSensitiveInformationResultEntryBuilder,
 ) -> crate::types::builders::GuardrailChecksSensitiveInformationResultEntryBuilder {
@@ -460,6 +520,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn audio_block_correct_errors(
     mut builder: crate::types::builders::AudioBlockBuilder,
 ) -> crate::types::builders::AudioBlockBuilder {
@@ -472,6 +533,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn cache_point_block_correct_errors(
     mut builder: crate::types::builders::CachePointBlockBuilder,
 ) -> crate::types::builders::CachePointBlockBuilder {
@@ -481,6 +543,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn document_block_correct_errors(
     mut builder: crate::types::builders::DocumentBlockBuilder,
 ) -> crate::types::builders::DocumentBlockBuilder {
@@ -493,6 +556,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_content_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailContentFilterBuilder,
 ) -> crate::types::builders::GuardrailContentFilterBuilder {
@@ -514,6 +582,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_contextual_grounding_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailContextualGroundingFilterBuilder,
 ) -> crate::types::builders::GuardrailContextualGroundingFilterBuilder {
@@ -536,6 +609,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_custom_word_correct_errors(
     mut builder: crate::types::builders::GuardrailCustomWordBuilder,
 ) -> crate::types::builders::GuardrailCustomWordBuilder {
@@ -550,6 +628,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_managed_word_correct_errors(
     mut builder: crate::types::builders::GuardrailManagedWordBuilder,
 ) -> crate::types::builders::GuardrailManagedWordBuilder {
@@ -569,6 +652,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_pii_entity_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailPiiEntityFilterBuilder,
 ) -> crate::types::builders::GuardrailPiiEntityFilterBuilder {
@@ -586,6 +674,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_regex_filter_correct_errors(
     mut builder: crate::types::builders::GuardrailRegexFilterBuilder,
 ) -> crate::types::builders::GuardrailRegexFilterBuilder {
@@ -597,6 +690,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub(crate) fn guardrail_topic_correct_errors(
     mut builder: crate::types::builders::GuardrailTopicBuilder,
 ) -> crate::types::builders::GuardrailTopicBuilder {
@@ -614,6 +712,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn image_block_correct_errors(
     mut builder: crate::types::builders::ImageBlockBuilder,
 ) -> crate::types::builders::ImageBlockBuilder {
@@ -626,6 +725,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn image_block_start_correct_errors(
     mut builder: crate::types::builders::ImageBlockStartBuilder,
 ) -> crate::types::builders::ImageBlockStartBuilder {
@@ -635,6 +735,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn search_result_block_correct_errors(
     mut builder: crate::types::builders::SearchResultBlockBuilder,
 ) -> crate::types::builders::SearchResultBlockBuilder {
@@ -650,6 +751,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_addition_block_correct_errors(
     mut builder: crate::types::builders::ToolAdditionBlockBuilder,
 ) -> crate::types::builders::ToolAdditionBlockBuilder {
@@ -662,6 +764,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_removal_block_correct_errors(
     mut builder: crate::types::builders::ToolRemovalBlockBuilder,
 ) -> crate::types::builders::ToolRemovalBlockBuilder {
@@ -674,6 +777,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_result_block_correct_errors(
     mut builder: crate::types::builders::ToolResultBlockBuilder,
 ) -> crate::types::builders::ToolResultBlockBuilder {
@@ -686,6 +790,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn tool_result_block_start_correct_errors(
     mut builder: crate::types::builders::ToolResultBlockStartBuilder,
 ) -> crate::types::builders::ToolResultBlockStartBuilder {
@@ -695,6 +800,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn tool_use_block_correct_errors(
     mut builder: crate::types::builders::ToolUseBlockBuilder,
 ) -> crate::types::builders::ToolUseBlockBuilder {
@@ -710,6 +816,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn tool_use_block_delta_correct_errors(
     mut builder: crate::types::builders::ToolUseBlockDeltaBuilder,
 ) -> crate::types::builders::ToolUseBlockDeltaBuilder {
@@ -719,6 +826,7 @@
     builder
 }

+#[cfg(feature = "op_converse_stream")]
 pub(crate) fn tool_use_block_start_correct_errors(
     mut builder: crate::types::builders::ToolUseBlockStartBuilder,
 ) -> crate::types::builders::ToolUseBlockStartBuilder {
@@ -731,6 +839,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn video_block_correct_errors(
     mut builder: crate::types::builders::VideoBlockBuilder,
 ) -> crate::types::builders::VideoBlockBuilder {
@@ -743,6 +852,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn citations_config_correct_errors(
     mut builder: crate::types::builders::CitationsConfigBuilder,
 ) -> crate::types::builders::CitationsConfigBuilder {
@@ -752,6 +862,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn guardrail_converse_image_block_correct_errors(
     mut builder: crate::types::builders::GuardrailConverseImageBlockBuilder,
 ) -> crate::types::builders::GuardrailConverseImageBlockBuilder {
@@ -766,6 +877,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn guardrail_converse_text_block_correct_errors(
     mut builder: crate::types::builders::GuardrailConverseTextBlockBuilder,
 ) -> crate::types::builders::GuardrailConverseTextBlockBuilder {
@@ -775,6 +887,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn reasoning_text_block_correct_errors(
     mut builder: crate::types::builders::ReasoningTextBlockBuilder,
 ) -> crate::types::builders::ReasoningTextBlockBuilder {
@@ -784,6 +897,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn s3_location_correct_errors(
     mut builder: crate::types::builders::S3LocationBuilder,
 ) -> crate::types::builders::S3LocationBuilder {
@@ -793,6 +907,7 @@
     builder
 }

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub(crate) fn search_result_content_block_correct_errors(
     mut builder: crate::types::builders::SearchResultContentBlockBuilder,
 ) -> crate::types::builders::SearchResultContentBlockBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,818 +1,1662 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_get_async_invoke", feature = "op_list_async_invokes"))]
 pub use crate::types::_async_invoke_status::AsyncInvokeStatus;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::_async_invoke_output_data_config::AsyncInvokeOutputDataConfig;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_sort_async_invocation_by::SortAsyncInvocationBy;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_sort_order::SortOrder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_content_source::GuardrailContentSource;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_output_scope::GuardrailOutputScope;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_usage::GuardrailUsage;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_action::GuardrailAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_coverage::GuardrailCoverage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_config::GuardrailChecksConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_results::GuardrailChecksResults;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_usage_results::GuardrailChecksUsageResults;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_inference_configuration::InferenceConfiguration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_configuration::ToolConfiguration;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_guardrail_configuration::GuardrailConfiguration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_performance_configuration::PerformanceConfiguration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_service_tier::ServiceTier;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_config::OutputConfig;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_output::ConverseOutput;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_stop_reason::StopReason;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_token_usage::TokenUsage;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_metrics::ConverseMetrics;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_trace::ConverseTrace;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_guardrail_stream_configuration::GuardrailStreamConfiguration;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_output::ConverseStreamOutput;

+#[cfg(any(feature = "op_invoke_model", feature = "op_invoke_model_with_response_stream"))]
 pub use crate::types::_trace::Trace;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::_performance_config_latency::PerformanceConfigLatency;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::_service_tier_type::ServiceTierType;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_invoke_model_with_bidirectional_stream_input::InvokeModelWithBidirectionalStreamInput;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_invoke_model_with_bidirectional_stream_output::InvokeModelWithBidirectionalStreamOutput;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub use crate::types::_response_stream::ResponseStream;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_count_tokens_input::CountTokensInput;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::_async_invoke_s3_output_data_config::AsyncInvokeS3OutputDataConfig;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_async_invoke_summary::AsyncInvokeSummary;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::_tag::Tag;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_content_block::GuardrailContentBlock;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_output_content::GuardrailOutputContent;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_assessment::GuardrailAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_text_characters_coverage::GuardrailTextCharactersCoverage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_image_coverage::GuardrailImageCoverage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_message::GuardrailChecksMessage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_config::GuardrailChecksContentFilterConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_config::GuardrailChecksPromptAttackConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_config::GuardrailChecksSensitiveInformationConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result::GuardrailChecksContentFilterResult;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result::GuardrailChecksPromptAttackResult;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result::GuardrailChecksSensitiveInformationResult;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_usage::GuardrailChecksContentFilterUsage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_usage::GuardrailChecksPromptAttackUsage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_usage::GuardrailChecksSensitiveInformationUsage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_message::Message;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_system_content_block::SystemContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_choice::ToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_guardrail_trace::GuardrailTrace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_prompt_variable_values::PromptVariableValues;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format::OutputFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_guardrail_trace_assessment::GuardrailTraceAssessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_prompt_router_trace::PromptRouterTrace;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_guardrail_stream_processing_mode::GuardrailStreamProcessingMode;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_start_event::MessageStartEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_start_event::ContentBlockStartEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_delta_event::ContentBlockDeltaEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_stop_event::ContentBlockStopEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_stop_event::MessageStopEvent;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metadata_event::ConverseStreamMetadataEvent;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_input_payload_part::BidirectionalInputPayloadPart;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_output_payload_part::BidirectionalOutputPayloadPart;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub use crate::types::_payload_part::PayloadPart;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_invoke_model_tokens_request::InvokeModelTokensRequest;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_converse_tokens_request::ConverseTokensRequest;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_text_block::GuardrailTextBlock;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_block::GuardrailImageBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_policy_assessment::GuardrailTopicPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_policy_assessment::GuardrailContentPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_word_policy_assessment::GuardrailWordPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_sensitive_information_policy_assessment::GuardrailSensitiveInformationPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_policy_assessment::GuardrailContextualGroundingPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_policy_assessment::GuardrailAutomatedReasoningPolicyAssessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_invocation_metrics::GuardrailInvocationMetrics;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_applied_guardrail_details::AppliedGuardrailDetails;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_role::GuardrailChecksRole;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_conversation_role::ConversationRole;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_content_block::GuardrailConverseContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_point_block::CachePointBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool::Tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_auto_tool_choice::AutoToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_any_tool_choice::AnyToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_specific_tool_choice::SpecificToolChoice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format_type::OutputFormatType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format_structure::OutputFormatStructure;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_cache_detail::CacheDetail;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_start::ContentBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_delta::ContentBlockDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metrics::ConverseStreamMetrics;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_trace::ConverseStreamTrace;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_format::GuardrailImageFormat;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_source::GuardrailImageSource;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_ownership::GuardrailOwnership;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_block::GuardrailChecksContentBlock;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_category_config::GuardrailChecksContentFilterCategoryConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_category_config::GuardrailChecksPromptAttackCategoryConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_entity_config::GuardrailChecksSensitiveInformationEntityConfig;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result_entry::GuardrailChecksContentFilterResultEntry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result_entry::GuardrailChecksPromptAttackResultEntry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result_entry::GuardrailChecksSensitiveInformationResultEntry;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_content_block::ContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_text_block::GuardrailConverseTextBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_block::GuardrailConverseImageBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_point_type::CachePointType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_ttl::CacheTtl;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_specification::ToolSpecification;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_system_tool::SystemTool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_json_schema_definition::JsonSchemaDefinition;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_start::ToolUseBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_result_block_start::ToolResultBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_start::ImageBlockStart;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_delta::ToolUseBlockDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_reasoning_content_block_delta::ReasoningContentBlockDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citations_delta::CitationsDelta;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_delta::ImageBlockDelta;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_content_qualifier::GuardrailContentQualifier;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic::GuardrailTopic;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter::GuardrailContentFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_custom_word::GuardrailCustomWord;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_managed_word::GuardrailManagedWord;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_pii_entity_filter::GuardrailPiiEntityFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_regex_filter::GuardrailRegexFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_filter::GuardrailContextualGroundingFilter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_finding::GuardrailAutomatedReasoningFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_origin::GuardrailOrigin;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_category::GuardrailChecksContentFilterCategory;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_category::GuardrailChecksPromptAttackCategory;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_entity_type::GuardrailChecksSensitiveInformationEntityType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_block::ImageBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_block::DocumentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_block::VideoBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_block::AudioBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_use_block::ToolUseBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_block::ToolResultBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_reasoning_content_block::ReasoningContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_content_block::CitationsContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_block::SearchResultBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_addition_block::ToolAdditionBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_removal_block::ToolRemovalBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_format::GuardrailConverseImageFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_source::GuardrailConverseImageSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_input_schema::ToolInputSchema;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_use_type::ToolUseType;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_status::ToolResultStatus;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_format::ImageFormat;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_result_block_delta::ToolResultBlockDelta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation_location::CitationLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_source::ImageSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_error_block::ErrorBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_type::GuardrailTopicType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_policy_action::GuardrailTopicPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter_type::GuardrailContentFilterType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter_confidence::GuardrailContentFilterConfidence;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter_strength::GuardrailContentFilterStrength;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_policy_action::GuardrailContentPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_word_policy_action::GuardrailWordPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_managed_word_type::GuardrailManagedWordType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_pii_entity_type::GuardrailPiiEntityType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_sensitive_information_policy_action::GuardrailSensitiveInformationPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_filter_type::GuardrailContextualGroundingFilterType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_policy_action::GuardrailContextualGroundingPolicyAction;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_valid_finding::GuardrailAutomatedReasoningValidFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_invalid_finding::GuardrailAutomatedReasoningInvalidFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_satisfiable_finding::GuardrailAutomatedReasoningSatisfiableFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_impossible_finding::GuardrailAutomatedReasoningImpossibleFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_ambiguous_finding::GuardrailAutomatedReasoningTranslationAmbiguousFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_too_complex_finding::GuardrailAutomatedReasoningTooComplexFinding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_no_translations_finding::GuardrailAutomatedReasoningNoTranslationsFinding;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_format::DocumentFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_source::DocumentSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_config::CitationsConfig;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_format::VideoFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_source::VideoSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_format::AudioFormat;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_source::AudioSource;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_reasoning_text_block::ReasoningTextBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_reference::ToolReference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_content_qualifier::GuardrailConverseContentQualifier;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citation_source_content_delta::CitationSourceContentDelta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_web_location::WebLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_char_location::DocumentCharLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_page_location::DocumentPageLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_chunk_location::DocumentChunkLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_location::SearchResultLocation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_s3_location::S3Location;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation::GuardrailAutomatedReasoningTranslation;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_scenario::GuardrailAutomatedReasoningScenario;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_logic_warning::GuardrailAutomatedReasoningLogicWarning;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_content_block::ToolResultContentBlock;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation_generated_content::CitationGeneratedContent;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation::Citation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_content_block::SearchResultContentBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_rule::GuardrailAutomatedReasoningRule;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_logic_warning_type::GuardrailAutomatedReasoningLogicWarningType;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_option::GuardrailAutomatedReasoningTranslationOption;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_content_block::DocumentContentBlock;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_statement::GuardrailAutomatedReasoningStatement;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_input_text_reference::GuardrailAutomatedReasoningInputTextReference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation_source_content::CitationSourceContent;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _any_tool_choice;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _applied_guardrail_details;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _async_invoke_output_data_config;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _async_invoke_s3_output_data_config;

+#[cfg(any(feature = "op_get_async_invoke", feature = "op_list_async_invokes"))]
 mod _async_invoke_status;

+#[cfg(feature = "op_list_async_invokes")]
 mod _async_invoke_summary;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _audio_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _audio_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _audio_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _auto_tool_choice;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _bidirectional_input_payload_part;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _bidirectional_output_payload_part;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _cache_detail;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _cache_point_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _cache_point_type;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _cache_ttl;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation_generated_content;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citation_source_content;

+#[cfg(feature = "op_converse_stream")]
 mod _citation_source_content_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citations_config;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _citations_content_block;

+#[cfg(feature = "op_converse_stream")]
 mod _citations_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _content_block;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_delta_event;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_start;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_start_event;

+#[cfg(feature = "op_converse_stream")]
 mod _content_block_stop_event;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _conversation_role;

+#[cfg(feature = "op_converse")]
 mod _converse_metrics;

+#[cfg(feature = "op_converse")]
 mod _converse_output;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_metadata_event;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_metrics;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_output;

+#[cfg(feature = "op_converse_stream")]
 mod _converse_stream_trace;

+#[cfg(feature = "op_count_tokens")]
 mod _converse_tokens_request;

+#[cfg(feature = "op_converse")]
 mod _converse_trace;

+#[cfg(feature = "op_count_tokens")]
 mod _count_tokens_input;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_char_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_chunk_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_page_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _document_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _error_block;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_impossible_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_input_text_reference;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_invalid_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_logic_warning;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_logic_warning_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_no_translations_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_rule;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_satisfiable_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_scenario;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_statement;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_too_complex_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_translation;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_translation_ambiguous_finding;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_translation_option;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_automated_reasoning_valid_finding;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_block;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_category;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_content_filter_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_message;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_category;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_category_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_prompt_attack_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_results;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_role;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_entity_config;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_entity_type;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_result;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_result_entry;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_sensitive_information_usage;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 mod _guardrail_checks_usage_results;

+#[cfg(feature = "op_converse")]
 mod _guardrail_configuration;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_content_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter_confidence;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter_strength;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_filter_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_content_policy_assessment;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_content_qualifier;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_content_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_filter_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_contextual_grounding_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_content_qualifier;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_image_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_image_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_image_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _guardrail_converse_text_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_coverage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_custom_word;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_image_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_image_coverage;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_image_format;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_image_source;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_invocation_metrics;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_managed_word;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_managed_word_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_origin;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_output_content;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_output_scope;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_ownership;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_pii_entity_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_pii_entity_type;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_regex_filter;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_sensitive_information_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_sensitive_information_policy_assessment;

+#[cfg(feature = "op_converse_stream")]
 mod _guardrail_stream_configuration;

+#[cfg(feature = "op_converse_stream")]
 mod _guardrail_stream_processing_mode;

+#[cfg(feature = "op_apply_guardrail")]
 mod _guardrail_text_block;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_text_characters_coverage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic_policy_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_topic_type;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _guardrail_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _guardrail_trace_assessment;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_usage;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_word_policy_action;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 mod _guardrail_word_policy_assessment;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _image_block;

+#[cfg(feature = "op_converse_stream")]
 mod _image_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _image_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _image_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _image_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _inference_configuration;

+#[cfg(feature = "op_count_tokens")]
 mod _invoke_model_tokens_request;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _invoke_model_with_bidirectional_stream_input;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 mod _invoke_model_with_bidirectional_stream_output;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _json_schema_definition;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _message;

+#[cfg(feature = "op_converse_stream")]
 mod _message_start_event;

+#[cfg(feature = "op_converse_stream")]
 mod _message_stop_event;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_config;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_format_structure;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _output_format_type;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 mod _payload_part;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _performance_config_latency;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _performance_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _prompt_router_trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _prompt_variable_values;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _reasoning_content_block;

+#[cfg(feature = "op_converse_stream")]
 mod _reasoning_content_block_delta;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _reasoning_text_block;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 mod _response_stream;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _s3_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _search_result_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _search_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _search_result_location;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _service_tier;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _service_tier_type;

+#[cfg(feature = "op_list_async_invokes")]
 mod _sort_async_invocation_by;

+#[cfg(feature = "op_list_async_invokes")]
 mod _sort_order;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _specific_tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _stop_reason;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _system_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _system_tool;

+#[cfg(feature = "op_start_async_invoke")]
 mod _tag;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 mod _token_usage;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_addition_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_choice;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_configuration;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_input_schema;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_reference;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_removal_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_result_block;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_result_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_result_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_result_content_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_result_status;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_specification;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_use_block;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_use_block_delta;

+#[cfg(feature = "op_converse_stream")]
 mod _tool_use_block_start;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _tool_use_type;

+#[cfg(any(feature = "op_invoke_model", feature = "op_invoke_model_with_response_stream"))]
 mod _trace;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _video_block;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _video_format;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _video_source;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 mod _web_location;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,250 +1,515 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_usage::GuardrailUsageBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_coverage::GuardrailCoverageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_config::GuardrailChecksConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_results::GuardrailChecksResultsBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_usage_results::GuardrailChecksUsageResultsBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_inference_configuration::InferenceConfigurationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_configuration::ToolConfigurationBuilder;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_guardrail_configuration::GuardrailConfigurationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_performance_configuration::PerformanceConfigurationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_service_tier::ServiceTierBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_config::OutputConfigBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_token_usage::TokenUsageBuilder;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_metrics::ConverseMetricsBuilder;

+#[cfg(feature = "op_converse")]
 pub use crate::types::_converse_trace::ConverseTraceBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_guardrail_stream_configuration::GuardrailStreamConfigurationBuilder;

+#[cfg(any(
+    feature = "op_get_async_invoke",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::_async_invoke_s3_output_data_config::AsyncInvokeS3OutputDataConfigBuilder;

+#[cfg(feature = "op_list_async_invokes")]
 pub use crate::types::_async_invoke_summary::AsyncInvokeSummaryBuilder;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_output_content::GuardrailOutputContentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_assessment::GuardrailAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_text_characters_coverage::GuardrailTextCharactersCoverageBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_image_coverage::GuardrailImageCoverageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_message::GuardrailChecksMessageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_config::GuardrailChecksContentFilterConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_config::GuardrailChecksPromptAttackConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_config::GuardrailChecksSensitiveInformationConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result::GuardrailChecksContentFilterResultBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result::GuardrailChecksPromptAttackResultBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result::GuardrailChecksSensitiveInformationResultBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_usage::GuardrailChecksContentFilterUsageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_usage::GuardrailChecksPromptAttackUsageBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_usage::GuardrailChecksSensitiveInformationUsageBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_message::MessageBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_output_format::OutputFormatBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_guardrail_trace_assessment::GuardrailTraceAssessmentBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_prompt_router_trace::PromptRouterTraceBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_start_event::MessageStartEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_start_event::ContentBlockStartEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_delta_event::ContentBlockDeltaEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_content_block_stop_event::ContentBlockStopEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_message_stop_event::MessageStopEventBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metadata_event::ConverseStreamMetadataEventBuilder;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_input_payload_part::BidirectionalInputPayloadPartBuilder;

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 pub use crate::types::_bidirectional_output_payload_part::BidirectionalOutputPayloadPartBuilder;

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 pub use crate::types::_payload_part::PayloadPartBuilder;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_invoke_model_tokens_request::InvokeModelTokensRequestBuilder;

+#[cfg(feature = "op_count_tokens")]
 pub use crate::types::_converse_tokens_request::ConverseTokensRequestBuilder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_text_block::GuardrailTextBlockBuilder;

+#[cfg(feature = "op_apply_guardrail")]
 pub use crate::types::_guardrail_image_block::GuardrailImageBlockBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic_policy_assessment::GuardrailTopicPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_policy_assessment::GuardrailContentPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_word_policy_assessment::GuardrailWordPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_sensitive_information_policy_assessment::GuardrailSensitiveInformationPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_policy_assessment::GuardrailContextualGroundingPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_policy_assessment::GuardrailAutomatedReasoningPolicyAssessmentBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_invocation_metrics::GuardrailInvocationMetricsBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_applied_guardrail_details::AppliedGuardrailDetailsBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_cache_point_block::CachePointBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_auto_tool_choice::AutoToolChoiceBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_any_tool_choice::AnyToolChoiceBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_specific_tool_choice::SpecificToolChoiceBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_cache_detail::CacheDetailBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_metrics::ConverseStreamMetricsBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_converse_stream_trace::ConverseStreamTraceBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_category_config::GuardrailChecksContentFilterCategoryConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_category_config::GuardrailChecksPromptAttackCategoryConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_entity_config::GuardrailChecksSensitiveInformationEntityConfigBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_content_filter_result_entry::GuardrailChecksContentFilterResultEntryBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_prompt_attack_result_entry::GuardrailChecksPromptAttackResultEntryBuilder;

+#[cfg(feature = "op_invoke_guardrail_checks")]
 pub use crate::types::_guardrail_checks_sensitive_information_result_entry::GuardrailChecksSensitiveInformationResultEntryBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_text_block::GuardrailConverseTextBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_guardrail_converse_image_block::GuardrailConverseImageBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_specification::ToolSpecificationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_system_tool::SystemToolBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream"))]
 pub use crate::types::_json_schema_definition::JsonSchemaDefinitionBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_start::ToolUseBlockStartBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_result_block_start::ToolResultBlockStartBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_start::ImageBlockStartBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_tool_use_block_delta::ToolUseBlockDeltaBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citations_delta::CitationsDeltaBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_image_block_delta::ImageBlockDeltaBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_topic::GuardrailTopicBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_content_filter::GuardrailContentFilterBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_custom_word::GuardrailCustomWordBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_managed_word::GuardrailManagedWordBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_pii_entity_filter::GuardrailPiiEntityFilterBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_regex_filter::GuardrailRegexFilterBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_contextual_grounding_filter::GuardrailContextualGroundingFilterBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_image_block::ImageBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_block::DocumentBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_video_block::VideoBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_audio_block::AudioBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_use_block::ToolUseBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_result_block::ToolResultBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_content_block::CitationsContentBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_block::SearchResultBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_addition_block::ToolAdditionBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_removal_block::ToolRemovalBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_error_block::ErrorBlockBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_valid_finding::GuardrailAutomatedReasoningValidFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_invalid_finding::GuardrailAutomatedReasoningInvalidFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_satisfiable_finding::GuardrailAutomatedReasoningSatisfiableFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_impossible_finding::GuardrailAutomatedReasoningImpossibleFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_ambiguous_finding::GuardrailAutomatedReasoningTranslationAmbiguousFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_too_complex_finding::GuardrailAutomatedReasoningTooComplexFindingBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_no_translations_finding::GuardrailAutomatedReasoningNoTranslationsFindingBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citations_config::CitationsConfigBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_reasoning_text_block::ReasoningTextBlockBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_tool_reference::ToolReferenceBuilder;

+#[cfg(feature = "op_converse_stream")]
 pub use crate::types::_citation_source_content_delta::CitationSourceContentDeltaBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_web_location::WebLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_char_location::DocumentCharLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_page_location::DocumentPageLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_document_chunk_location::DocumentChunkLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_location::SearchResultLocationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_s3_location::S3LocationBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation::GuardrailAutomatedReasoningTranslationBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_scenario::GuardrailAutomatedReasoningScenarioBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_logic_warning::GuardrailAutomatedReasoningLogicWarningBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_citation::CitationBuilder;

+#[cfg(any(feature = "op_converse", feature = "op_converse_stream", feature = "op_count_tokens"))]
 pub use crate::types::_search_result_content_block::SearchResultContentBlockBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_rule::GuardrailAutomatedReasoningRuleBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_translation_option::GuardrailAutomatedReasoningTranslationOptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_statement::GuardrailAutomatedReasoningStatementBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream"
+))]
 pub use crate::types::_guardrail_automated_reasoning_input_text_reference::GuardrailAutomatedReasoningInputTextReferenceBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,28 +1,136 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_validation_exception::ValidationException;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededException;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableException;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_error_exception::ModelErrorException;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_not_ready_exception::ModelNotReadyException;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_timeout_exception::ModelTimeoutException;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_stream_error_exception::ModelStreamErrorException;

+#[cfg(feature = "op_converse_stream")]
 /// Error type for the `ConverseStreamOutputError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -48,6 +156,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_converse_stream")]
 impl ConverseStreamOutputError {
     /// Creates the `ConverseStreamOutputError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -103,6 +212,7 @@
         matches!(self, Self::ServiceUnavailableException(_))
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::std::error::Error for ConverseStreamOutputError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -115,6 +225,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::std::fmt::Display for ConverseStreamOutputError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -135,6 +246,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for ConverseStreamOutputError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -143,6 +255,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for ConverseStreamOutputError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -165,6 +278,7 @@
         }
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for ConverseStreamOutputError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -176,6 +290,7 @@
         })
     }
 }
+#[cfg(feature = "op_converse_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::ConverseStreamOutputError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -182,6 +297,7 @@
     }
 }

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 /// Error type for the `InvokeModelWithBidirectionalStreamInputError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -197,6 +313,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl InvokeModelWithBidirectionalStreamInputError {
     /// Creates the `InvokeModelWithBidirectionalStreamInputError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -227,6 +344,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::error::Error for InvokeModelWithBidirectionalStreamInputError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -234,6 +352,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::fmt::Display for InvokeModelWithBidirectionalStreamInputError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -249,6 +368,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for InvokeModelWithBidirectionalStreamInputError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -257,6 +377,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for InvokeModelWithBidirectionalStreamInputError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -264,6 +385,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for InvokeModelWithBidirectionalStreamInputError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -275,6 +397,7 @@
         })
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::InvokeModelWithBidirectionalStreamInputError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -281,6 +404,7 @@
     }
 }

+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 /// Error type for the `InvokeModelWithBidirectionalStreamOutputError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -308,6 +432,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl InvokeModelWithBidirectionalStreamOutputError {
     /// Creates the `InvokeModelWithBidirectionalStreamOutputError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -368,6 +493,7 @@
         matches!(self, Self::ServiceUnavailableException(_))
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::error::Error for InvokeModelWithBidirectionalStreamOutputError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -381,6 +507,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::std::fmt::Display for InvokeModelWithBidirectionalStreamOutputError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -402,6 +529,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for InvokeModelWithBidirectionalStreamOutputError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -410,6 +538,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for InvokeModelWithBidirectionalStreamOutputError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -435,6 +564,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for InvokeModelWithBidirectionalStreamOutputError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -446,6 +576,7 @@
         })
     }
 }
+#[cfg(feature = "op_invoke_model_with_bidirectional_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::InvokeModelWithBidirectionalStreamOutputError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -452,6 +583,7 @@
     }
 }

+#[cfg(feature = "op_invoke_model_with_response_stream")]
 /// Error type for the `ResponseStreamError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -479,6 +611,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ResponseStreamError {
     /// Creates the `ResponseStreamError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -539,6 +672,7 @@
         matches!(self, Self::ServiceUnavailableException(_))
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::std::error::Error for ResponseStreamError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -552,6 +686,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::std::fmt::Display for ResponseStreamError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -573,6 +708,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for ResponseStreamError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -581,6 +717,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for ResponseStreamError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -606,6 +743,7 @@
         }
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for ResponseStreamError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -617,6 +755,7 @@
         })
     }
 }
+#[cfg(feature = "op_invoke_model_with_response_stream")]
 impl ::aws_types::request_id::RequestId for crate::types::error::ResponseStreamError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -623,28 +762,135 @@
     }
 }

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _access_denied_exception;

+#[cfg(feature = "op_start_async_invoke")]
 mod _conflict_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _internal_server_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_not_ready_exception;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_stream_error_exception;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 mod _model_timeout_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 mod _service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 mod _service_unavailable_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _throttling_exception;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 mod _validation_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,24 +1,131 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_get_async_invoke",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_list_async_invokes",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_validation_exception::ValidationExceptionBuilder;

+#[cfg(feature = "op_start_async_invoke")]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_apply_guardrail",
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_count_tokens",
+    feature = "op_invoke_guardrail_checks",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream",
+    feature = "op_start_async_invoke"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_error_exception::ModelErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_not_ready_exception::ModelNotReadyExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse",
+    feature = "op_converse_stream",
+    feature = "op_invoke_model",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_timeout_exception::ModelTimeoutExceptionBuilder;

+#[cfg(any(
+    feature = "op_converse_stream",
+    feature = "op_invoke_model_with_bidirectional_stream",
+    feature = "op_invoke_model_with_response_stream"
+))]
 pub use crate::types::error::_model_stream_error_exception::ModelStreamErrorExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
