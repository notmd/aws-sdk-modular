# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/sqs`
- model: `aws-models/sqs.json`
- package: `aws-sdk-sqs`
- library: `aws_sdk_sqs`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_add_permission`: `AddPermission`
- `op_cancel_message_move_task`: `CancelMessageMoveTask`
- `op_change_message_visibility`: `ChangeMessageVisibility`
- `op_change_message_visibility_batch`: `ChangeMessageVisibilityBatch`
- `op_create_queue`: `CreateQueue`
- `op_delete_message`: `DeleteMessage`
- `op_delete_message_batch`: `DeleteMessageBatch`
- `op_delete_queue`: `DeleteQueue`
- `op_get_queue_attributes`: `GetQueueAttributes`
- `op_get_queue_url`: `GetQueueUrl`
- `op_list_dead_letter_source_queues`: `ListDeadLetterSourceQueues`
- `op_list_message_move_tasks`: `ListMessageMoveTasks`
- `op_list_queues`: `ListQueues`
- `op_list_queue_tags`: `ListQueueTags`
- `op_purge_queue`: `PurgeQueue`
- `op_receive_message`: `ReceiveMessage`
- `op_remove_permission`: `RemovePermission`
- `op_send_message`: `SendMessage`
- `op_send_message_batch`: `SendMessageBatch`
- `op_set_queue_attributes`: `SetQueueAttributes`
- `op_start_message_move_task`: `StartMessageMoveTask`
- `op_tag_queue`: `TagQueue`
- `op_untag_queue`: `UntagQueue`

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

@@ -153,6 +133,29 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_add_permission = []
+op_cancel_message_move_task = []
+op_change_message_visibility = []
+op_change_message_visibility_batch = []
+op_create_queue = []
+op_delete_message = []
+op_delete_message_batch = []
+op_delete_queue = []
+op_get_queue_attributes = []
+op_get_queue_url = []
+op_list_dead_letter_source_queues = []
+op_list_message_move_tasks = []
+op_list_queues = []
+op_list_queue_tags = []
+op_purge_queue = []
+op_receive_message = []
+op_remove_permission = []
+op_send_message = []
+op_send_message_batch = []
+op_set_queue_attributes = []
+op_start_message_move_task = []
+op_tag_queue = []
+op_untag_queue = []

 [hints]
 mostly-unused = true
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,14 +136,19 @@
     }
 }

+#[cfg(feature = "op_add_permission")]
 mod add_permission;

+#[cfg(feature = "op_cancel_message_move_task")]
 mod cancel_message_move_task;

+#[cfg(feature = "op_change_message_visibility")]
 mod change_message_visibility;

+#[cfg(feature = "op_change_message_visibility_batch")]
 mod change_message_visibility_batch;

+#[cfg(feature = "op_create_queue")]
 mod create_queue;

 /// Operation customization and supporting types.
@@ -173,38 +178,56 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_message")]
 mod delete_message;

+#[cfg(feature = "op_delete_message_batch")]
 mod delete_message_batch;

+#[cfg(feature = "op_delete_queue")]
 mod delete_queue;

+#[cfg(feature = "op_get_queue_attributes")]
 mod get_queue_attributes;

+#[cfg(feature = "op_get_queue_url")]
 mod get_queue_url;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 mod list_dead_letter_source_queues;

+#[cfg(feature = "op_list_message_move_tasks")]
 mod list_message_move_tasks;

+#[cfg(feature = "op_list_queue_tags")]
 mod list_queue_tags;

+#[cfg(feature = "op_list_queues")]
 mod list_queues;

+#[cfg(feature = "op_purge_queue")]
 mod purge_queue;

+#[cfg(feature = "op_receive_message")]
 mod receive_message;

+#[cfg(feature = "op_remove_permission")]
 mod remove_permission;

+#[cfg(feature = "op_send_message")]
 mod send_message;

+#[cfg(feature = "op_send_message_batch")]
 mod send_message_batch;

+#[cfg(feature = "op_set_queue_attributes")]
 mod set_queue_attributes;

+#[cfg(feature = "op_start_message_move_task")]
 mod start_message_move_task;

+#[cfg(feature = "op_tag_queue")]
 mod tag_queue;

+#[cfg(feature = "op_untag_queue")]
 mod untag_queue;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,31 +3,120 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>Two or more batch entries in the request have the same <code>Id</code>.</p>
     BatchEntryIdsNotDistinct(crate::types::error::BatchEntryIdsNotDistinct),
+    #[cfg(feature = "op_send_message_batch")]
     /// <p>The length of all the messages put together is more than the limit.</p>
     BatchRequestTooLong(crate::types::error::BatchRequestTooLong),
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The batch request doesn't contain any entries.</p>
     EmptyBatchRequest(crate::types::error::EmptyBatchRequest),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>The specified ID is invalid.</p>
     InvalidAddress(crate::types::error::InvalidAddress),
+    #[cfg(any(
+        feature = "op_create_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_set_queue_attributes"
+    ))]
     /// <p>The specified attribute doesn't exist.</p>
     InvalidAttributeName(crate::types::error::InvalidAttributeName),
+    #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
     /// <p>A queue attribute value is invalid.</p>
     InvalidAttributeValue(crate::types::error::InvalidAttributeValue),
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The <code>Id</code> of a batch entry in a batch request doesn't abide by the specification.</p>
     InvalidBatchEntryId(crate::types::error::InvalidBatchEntryId),
+    #[cfg(feature = "op_delete_message")]
     /// <p>The specified receipt handle isn't valid for the current version.</p>
     #[deprecated(note = "exception has been included in ReceiptHandleIsInvalid")]
     InvalidIdFormat(crate::types::error::InvalidIdFormat),
+    #[cfg(feature = "op_send_message")]
     /// <p>The message contains characters outside the allowed set.</p>
     InvalidMessageContents(crate::types::error::InvalidMessageContents),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>The request was not made over HTTPS or did not use SigV4 for signing.</p>
     InvalidSecurity(crate::types::error::InvalidSecurity),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The caller doesn't have the required KMS access.</p>
     KmsAccessDenied(crate::types::error::KmsAccessDenied),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was denied due to request throttling.</p>
     KmsDisabled(crate::types::error::KmsDisabled),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected for one of the following reasons:</p>
     /// <ul>
     /// <li>
@@ -36,28 +125,103 @@
     /// <p>The encryption algorithm or signing algorithm specified for the operation is incompatible with the type of key material in the KMS key (KeySpec).</p></li>
     /// </ul>
     KmsInvalidKeyUsage(crate::types::error::KmsInvalidKeyUsage),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected because the state of the specified resource is not valid for this request.</p>
     KmsInvalidState(crate::types::error::KmsInvalidState),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected because the specified entity or resource could not be found.</p>
     KmsNotFound(crate::types::error::KmsNotFound),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected because the specified key policy isn't syntactically or semantically correct.</p>
     KmsOptInRequired(crate::types::error::KmsOptInRequired),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>Amazon Web Services KMS throttles requests for the following conditions.</p>
     KmsThrottled(crate::types::error::KmsThrottled),
+    #[cfg(feature = "op_change_message_visibility")]
     /// <p>The specified message isn't in flight.</p>
     MessageNotInflight(crate::types::error::MessageNotInflight),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_receive_message",
+        feature = "op_set_queue_attributes"
+    ))]
     /// <p>The specified action violates a limit. For example, <code>ReceiveMessage</code> returns this error if the maximum number of in flight messages is reached and <code>AddPermission</code> returns this error if the maximum number of permissions for the queue is reached.</p>
     OverLimit(crate::types::error::OverLimit),
+    #[cfg(feature = "op_purge_queue")]
     /// <p>Indicates that the specified queue previously received a <code>PurgeQueue</code> request within the last 60 seconds (the time it can take to delete the messages in the queue).</p>
     PurgeQueueInProgress(crate::types::error::PurgeQueueInProgress),
+    #[cfg(feature = "op_create_queue")]
     /// <p>You must wait 60 seconds after deleting a queue before you can create another queue with the same name.</p>
     QueueDeletedRecently(crate::types::error::QueueDeletedRecently),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_queue_tags",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>Ensure that the <code>QueueUrl</code> is correct and that the queue has not been deleted.</p>
     QueueDoesNotExist(crate::types::error::QueueDoesNotExist),
+    #[cfg(feature = "op_create_queue")]
     /// <p>A queue with this name already exists. Amazon SQS returns this error only if the request includes attributes whose values differ from those of the existing queue.</p>
     QueueNameExists(crate::types::error::QueueNameExists),
+    #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
     /// <p>The specified receipt handle isn't valid.</p>
     ReceiptHandleIsInvalid(crate::types::error::ReceiptHandleIsInvalid),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>The request was denied due to request throttling.</p>
     /// <ul>
     /// <li>
@@ -66,10 +230,45 @@
     /// <p>Ensure that the request rate is within the Amazon SQS limits for sending messages. For more information, see <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-quotas.html#quotas-requests">Amazon SQS quotas</a> in the <i>Amazon SQS Developer Guide</i>.</p></li>
     /// </ul>
     RequestThrottled(crate::types::error::RequestThrottled),
+    #[cfg(any(
+        feature = "op_cancel_message_move_task",
+        feature = "op_list_message_move_tasks",
+        feature = "op_start_message_move_task"
+    ))]
     /// <p>One or more specified resources don't exist.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The batch request contains more entries than permissible. For Amazon SQS, the maximum number of entries you can include in a single <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SendMessageBatch.html">SendMessageBatch</a>, <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_DeleteMessageBatch.html">DeleteMessageBatch</a>, or <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_ChangeMessageVisibilityBatch.html">ChangeMessageVisibilityBatch</a> request is 10.</p>
     TooManyEntriesInBatchRequest(crate::types::error::TooManyEntriesInBatchRequest),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>Error code 400. Unsupported operation.</p>
     UnsupportedOperation(crate::types::error::UnsupportedOperation),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -86,33 +285,232 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::BatchEntryIdsNotDistinct(inner) => inner.fmt(f),
+            #[cfg(feature = "op_send_message_batch")]
             Error::BatchRequestTooLong(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::EmptyBatchRequest(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidAddress(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::InvalidAttributeName(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Error::InvalidAttributeValue(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::InvalidBatchEntryId(inner) => inner.fmt(f),
+            #[cfg(feature = "op_delete_message")]
             Error::InvalidIdFormat(inner) => inner.fmt(f),
+            #[cfg(feature = "op_send_message")]
             Error::InvalidMessageContents(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidSecurity(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsAccessDenied(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsDisabled(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidKeyUsage(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidState(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsNotFound(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsOptInRequired(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsThrottled(inner) => inner.fmt(f),
+            #[cfg(feature = "op_change_message_visibility")]
             Error::MessageNotInflight(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::OverLimit(inner) => inner.fmt(f),
+            #[cfg(feature = "op_purge_queue")]
             Error::PurgeQueueInProgress(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueDeletedRecently(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::QueueDoesNotExist(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueNameExists(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Error::ReceiptHandleIsInvalid(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::RequestThrottled(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::TooManyEntriesInBatchRequest(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::UnsupportedOperation(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -137,38 +535,238 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::BatchEntryIdsNotDistinct(inner) => inner.meta(),
+            #[cfg(feature = "op_send_message_batch")]
             Self::BatchRequestTooLong(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::EmptyBatchRequest(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidAddress(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::InvalidAttributeName(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Self::InvalidAttributeValue(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::InvalidBatchEntryId(inner) => inner.meta(),
+            #[cfg(feature = "op_delete_message")]
             Self::InvalidIdFormat(inner) => inner.meta(),
+            #[cfg(feature = "op_send_message")]
             Self::InvalidMessageContents(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidSecurity(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsAccessDenied(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsDisabled(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidKeyUsage(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidState(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsNotFound(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsOptInRequired(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsThrottled(inner) => inner.meta(),
+            #[cfg(feature = "op_change_message_visibility")]
             Self::MessageNotInflight(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::OverLimit(inner) => inner.meta(),
+            #[cfg(feature = "op_purge_queue")]
             Self::PurgeQueueInProgress(inner) => inner.meta(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueDeletedRecently(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::QueueDoesNotExist(inner) => inner.meta(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueNameExists(inner) => inner.meta(),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Self::ReceiptHandleIsInvalid(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::RequestThrottled(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::TooManyEntriesInBatchRequest(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::UnsupportedOperation(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::add_permission::AddPermissionError, R>>
     for Error
@@ -190,6 +788,7 @@
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl From<crate::operation::add_permission::AddPermissionError> for Error {
     fn from(err: crate::operation::add_permission::AddPermissionError) -> Self {
         match err {
@@ -211,6 +810,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_message_move_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -236,6 +836,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_message_move_task")]
 impl From<crate::operation::cancel_message_move_task::CancelMessageMoveTaskError> for Error {
     fn from(err: crate::operation::cancel_message_move_task::CancelMessageMoveTaskError) -> Self {
         match err {
@@ -260,6 +861,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -285,6 +887,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility")]
 impl From<crate::operation::change_message_visibility::ChangeMessageVisibilityError> for Error {
     fn from(err: crate::operation::change_message_visibility::ChangeMessageVisibilityError) -> Self {
         match err {
@@ -315,6 +918,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility_batch")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -340,6 +944,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility_batch")]
 impl From<crate::operation::change_message_visibility_batch::ChangeMessageVisibilityBatchError> for Error {
     fn from(err: crate::operation::change_message_visibility_batch::ChangeMessageVisibilityBatchError) -> Self {
         match err {
@@ -374,6 +979,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_queue::CreateQueueError, R>>
     for Error
 where
@@ -391,6 +997,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_queue")]
 impl From<crate::operation::create_queue::CreateQueueError> for Error {
     fn from(err: crate::operation::create_queue::CreateQueueError) -> Self {
         match err {
@@ -414,6 +1021,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_message::DeleteMessageError, R>>
     for Error
@@ -435,6 +1043,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message")]
 impl From<crate::operation::delete_message::DeleteMessageError> for Error {
     fn from(err: crate::operation::delete_message::DeleteMessageError) -> Self {
         match err {
@@ -461,6 +1070,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message_batch")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -486,6 +1096,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message_batch")]
 impl From<crate::operation::delete_message_batch::DeleteMessageBatchError> for Error {
     fn from(err: crate::operation::delete_message_batch::DeleteMessageBatchError) -> Self {
         match err {
@@ -522,6 +1133,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_queue::DeleteQueueError, R>>
     for Error
 where
@@ -539,6 +1151,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_queue")]
 impl From<crate::operation::delete_queue::DeleteQueueError> for Error {
     fn from(err: crate::operation::delete_queue::DeleteQueueError) -> Self {
         match err {
@@ -555,6 +1168,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -580,6 +1194,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_attributes")]
 impl From<crate::operation::get_queue_attributes::GetQueueAttributesError> for Error {
     fn from(err: crate::operation::get_queue_attributes::GetQueueAttributesError) -> Self {
         match err {
@@ -607,6 +1222,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_url")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_queue_url::GetQueueUrlError, R>>
     for Error
 where
@@ -624,6 +1240,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_url")]
 impl From<crate::operation::get_queue_url::GetQueueUrlError> for Error {
     fn from(err: crate::operation::get_queue_url::GetQueueUrlError) -> Self {
         match err {
@@ -642,6 +1259,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dead_letter_source_queues")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -667,6 +1285,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dead_letter_source_queues")]
 impl From<crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesError> for Error {
     fn from(err: crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesError) -> Self {
         match err {
@@ -691,6 +1310,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_message_move_tasks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -716,6 +1336,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_message_move_tasks")]
 impl From<crate::operation::list_message_move_tasks::ListMessageMoveTasksError> for Error {
     fn from(err: crate::operation::list_message_move_tasks::ListMessageMoveTasksError) -> Self {
         match err {
@@ -740,6 +1361,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queues")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_queues::ListQueuesError, R>>
     for Error
 where
@@ -757,6 +1379,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queues")]
 impl From<crate::operation::list_queues::ListQueuesError> for Error {
     fn from(err: crate::operation::list_queues::ListQueuesError) -> Self {
         match err {
@@ -770,6 +1393,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queue_tags")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_queue_tags::ListQueueTagsError, R>>
     for Error
@@ -791,6 +1415,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queue_tags")]
 impl From<crate::operation::list_queue_tags::ListQueueTagsError> for Error {
     fn from(err: crate::operation::list_queue_tags::ListQueueTagsError) -> Self {
         match err {
@@ -813,6 +1438,7 @@
         }
     }
 }
+#[cfg(feature = "op_purge_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::purge_queue::PurgeQueueError, R>>
     for Error
 where
@@ -830,6 +1456,7 @@
         }
     }
 }
+#[cfg(feature = "op_purge_queue")]
 impl From<crate::operation::purge_queue::PurgeQueueError> for Error {
     fn from(err: crate::operation::purge_queue::PurgeQueueError) -> Self {
         match err {
@@ -847,6 +1474,7 @@
         }
     }
 }
+#[cfg(feature = "op_receive_message")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::receive_message::ReceiveMessageError, R>>
     for Error
@@ -868,6 +1496,7 @@
         }
     }
 }
+#[cfg(feature = "op_receive_message")]
 impl From<crate::operation::receive_message::ReceiveMessageError> for Error {
     fn from(err: crate::operation::receive_message::ReceiveMessageError) -> Self {
         match err {
@@ -906,6 +1535,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -931,6 +1561,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl From<crate::operation::remove_permission::RemovePermissionError> for Error {
     fn from(err: crate::operation::remove_permission::RemovePermissionError) -> Self {
         match err {
@@ -953,6 +1584,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::send_message::SendMessageError, R>>
     for Error
 where
@@ -970,6 +1602,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message")]
 impl From<crate::operation::send_message::SendMessageError> for Error {
     fn from(err: crate::operation::send_message::SendMessageError) -> Self {
         match err {
@@ -998,6 +1631,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message_batch")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1023,6 +1657,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message_batch")]
 impl From<crate::operation::send_message_batch::SendMessageBatchError> for Error {
     fn from(err: crate::operation::send_message_batch::SendMessageBatchError) -> Self {
         match err {
@@ -1081,6 +1716,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_queue_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1106,6 +1742,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_queue_attributes")]
 impl From<crate::operation::set_queue_attributes::SetQueueAttributesError> for Error {
     fn from(err: crate::operation::set_queue_attributes::SetQueueAttributesError) -> Self {
         match err {
@@ -1139,6 +1776,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_message_move_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1164,6 +1802,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_message_move_task")]
 impl From<crate::operation::start_message_move_task::StartMessageMoveTaskError> for Error {
     fn from(err: crate::operation::start_message_move_task::StartMessageMoveTaskError) -> Self {
         match err {
@@ -1188,6 +1827,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_queue::TagQueueError, R>>
     for Error
 where
@@ -1205,6 +1845,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_queue")]
 impl From<crate::operation::tag_queue::TagQueueError> for Error {
     fn from(err: crate::operation::tag_queue::TagQueueError) -> Self {
         match err {
@@ -1219,6 +1860,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_queue::UntagQueueError, R>>
     for Error
 where
@@ -1236,6 +1878,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_queue")]
 impl From<crate::operation::untag_queue::UntagQueueError> for Error {
     fn from(err: crate::operation::untag_queue::UntagQueueError) -> Self {
         match err {
@@ -1253,33 +1896,232 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::BatchEntryIdsNotDistinct(inner) => inner.source(),
+            #[cfg(feature = "op_send_message_batch")]
             Error::BatchRequestTooLong(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::EmptyBatchRequest(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidAddress(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::InvalidAttributeName(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Error::InvalidAttributeValue(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::InvalidBatchEntryId(inner) => inner.source(),
+            #[cfg(feature = "op_delete_message")]
             Error::InvalidIdFormat(inner) => inner.source(),
+            #[cfg(feature = "op_send_message")]
             Error::InvalidMessageContents(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidSecurity(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsAccessDenied(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsDisabled(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidKeyUsage(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidState(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsNotFound(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsOptInRequired(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsThrottled(inner) => inner.source(),
+            #[cfg(feature = "op_change_message_visibility")]
             Error::MessageNotInflight(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::OverLimit(inner) => inner.source(),
+            #[cfg(feature = "op_purge_queue")]
             Error::PurgeQueueInProgress(inner) => inner.source(),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueDeletedRecently(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::QueueDoesNotExist(inner) => inner.source(),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueNameExists(inner) => inner.source(),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Error::ReceiptHandleIsInvalid(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::RequestThrottled(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::TooManyEntriesInBatchRequest(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::UnsupportedOperation(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -1288,33 +2130,232 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::BatchEntryIdsNotDistinct(e) => e.request_id(),
+            #[cfg(feature = "op_send_message_batch")]
             Self::BatchRequestTooLong(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::EmptyBatchRequest(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidAddress(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::InvalidAttributeName(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Self::InvalidAttributeValue(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::InvalidBatchEntryId(e) => e.request_id(),
+            #[cfg(feature = "op_delete_message")]
             Self::InvalidIdFormat(e) => e.request_id(),
+            #[cfg(feature = "op_send_message")]
             Self::InvalidMessageContents(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidSecurity(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsAccessDenied(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsDisabled(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidKeyUsage(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidState(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsNotFound(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsOptInRequired(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsThrottled(e) => e.request_id(),
+            #[cfg(feature = "op_change_message_visibility")]
             Self::MessageNotInflight(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::OverLimit(e) => e.request_id(),
+            #[cfg(feature = "op_purge_queue")]
             Self::PurgeQueueInProgress(e) => e.request_id(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueDeletedRecently(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::QueueDoesNotExist(e) => e.request_id(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueNameExists(e) => e.request_id(),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Self::ReceiptHandleIsInvalid(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::RequestThrottled(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::TooManyEntriesInBatchRequest(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::UnsupportedOperation(e) => e.request_id(),
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
+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) fn reflens_list_dead_letter_source_queues_output_output_next_token(
     input: &crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_queues")]
 pub(crate) fn reflens_list_queues_output_output_next_token(
     input: &crate::operation::list_queues::ListQueuesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) fn lens_list_dead_letter_source_queues_output_output_queue_urls(
     input: crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -26,6 +29,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_queues")]
 pub(crate) fn lens_list_queues_output_output_queue_urls(
     input: crate::operation::list_queues::ListQueuesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,71 +1,94 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_add_permission")]
 /// Types for the `AddPermission` operation.
 pub mod add_permission;

+#[cfg(feature = "op_cancel_message_move_task")]
 /// Types for the `CancelMessageMoveTask` operation.
 pub mod cancel_message_move_task;

+#[cfg(feature = "op_change_message_visibility")]
 /// Types for the `ChangeMessageVisibility` operation.
 pub mod change_message_visibility;

+#[cfg(feature = "op_change_message_visibility_batch")]
 /// Types for the `ChangeMessageVisibilityBatch` operation.
 pub mod change_message_visibility_batch;

+#[cfg(feature = "op_create_queue")]
 /// Types for the `CreateQueue` operation.
 pub mod create_queue;

+#[cfg(feature = "op_delete_message")]
 /// Types for the `DeleteMessage` operation.
 pub mod delete_message;

+#[cfg(feature = "op_delete_message_batch")]
 /// Types for the `DeleteMessageBatch` operation.
 pub mod delete_message_batch;

+#[cfg(feature = "op_delete_queue")]
 /// Types for the `DeleteQueue` operation.
 pub mod delete_queue;

+#[cfg(feature = "op_get_queue_attributes")]
 /// Types for the `GetQueueAttributes` operation.
 pub mod get_queue_attributes;

+#[cfg(feature = "op_get_queue_url")]
 /// Types for the `GetQueueUrl` operation.
 pub mod get_queue_url;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 /// Types for the `ListDeadLetterSourceQueues` operation.
 pub mod list_dead_letter_source_queues;

+#[cfg(feature = "op_list_message_move_tasks")]
 /// Types for the `ListMessageMoveTasks` operation.
 pub mod list_message_move_tasks;

+#[cfg(feature = "op_list_queue_tags")]
 /// Types for the `ListQueueTags` operation.
 pub mod list_queue_tags;

+#[cfg(feature = "op_list_queues")]
 /// Types for the `ListQueues` operation.
 pub mod list_queues;

+#[cfg(feature = "op_purge_queue")]
 /// Types for the `PurgeQueue` operation.
 pub mod purge_queue;

+#[cfg(feature = "op_receive_message")]
 /// Types for the `ReceiveMessage` operation.
 pub mod receive_message;

+#[cfg(feature = "op_remove_permission")]
 /// Types for the `RemovePermission` operation.
 pub mod remove_permission;

+#[cfg(feature = "op_send_message")]
 /// Types for the `SendMessage` operation.
 pub mod send_message;

+#[cfg(feature = "op_send_message_batch")]
 /// Types for the `SendMessageBatch` operation.
 pub mod send_message_batch;

+#[cfg(feature = "op_set_queue_attributes")]
 /// Types for the `SetQueueAttributes` operation.
 pub mod set_queue_attributes;

+#[cfg(feature = "op_start_message_move_task")]
 /// Types for the `StartMessageMoveTask` operation.
 pub mod start_message_move_task;

+#[cfg(feature = "op_tag_queue")]
 /// Types for the `TagQueue` operation.
 pub mod tag_queue;

+#[cfg(feature = "op_untag_queue")]
 /// Types for the `UntagQueue` operation.
 pub mod untag_queue;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,29 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +42,31 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -35,54 +85,103 @@
     Ok(builder)
 }

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission;

+#[cfg(feature = "op_cancel_message_move_task")]
 pub(crate) mod shape_cancel_message_move_task;

+#[cfg(feature = "op_change_message_visibility")]
 pub(crate) mod shape_change_message_visibility;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_create_queue;

+#[cfg(feature = "op_delete_message")]
 pub(crate) mod shape_delete_message;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch;

+#[cfg(feature = "op_delete_queue")]
 pub(crate) mod shape_delete_queue;

+#[cfg(feature = "op_get_queue_attributes")]
 pub(crate) mod shape_get_queue_attributes;

+#[cfg(feature = "op_get_queue_url")]
 pub(crate) mod shape_get_queue_url;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) mod shape_list_dead_letter_source_queues;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks;

+#[cfg(feature = "op_list_queue_tags")]
 pub(crate) mod shape_list_queue_tags;

+#[cfg(feature = "op_list_queues")]
 pub(crate) mod shape_list_queues;

+#[cfg(feature = "op_purge_queue")]
 pub(crate) mod shape_purge_queue;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_receive_message;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission;

+#[cfg(feature = "op_send_message")]
 pub(crate) mod shape_send_message;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch;

+#[cfg(feature = "op_set_queue_attributes")]
 pub(crate) mod shape_set_queue_attributes;

+#[cfg(feature = "op_start_message_move_task")]
 pub(crate) mod shape_start_message_move_task;

+#[cfg(feature = "op_tag_queue")]
 pub(crate) mod shape_tag_queue;

+#[cfg(feature = "op_untag_queue")]
 pub(crate) mod shape_untag_queue;

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -91,150 +190,415 @@
     }
 }

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_batch_entry_ids_not_distinct;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_batch_request_too_long;

+#[cfg(feature = "op_cancel_message_move_task")]
 pub(crate) mod shape_cancel_message_move_task_input;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_input;

+#[cfg(feature = "op_change_message_visibility")]
 pub(crate) mod shape_change_message_visibility_input;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_create_queue_input;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_input;

+#[cfg(feature = "op_delete_message")]
 pub(crate) mod shape_delete_message_input;

+#[cfg(feature = "op_delete_queue")]
 pub(crate) mod shape_delete_queue_input;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_empty_batch_request;

+#[cfg(feature = "op_get_queue_attributes")]
 pub(crate) mod shape_get_queue_attributes_input;

+#[cfg(feature = "op_get_queue_url")]
 pub(crate) mod shape_get_queue_url_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_invalid_address;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 pub(crate) mod shape_invalid_attribute_name;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 pub(crate) mod shape_invalid_attribute_value;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_invalid_batch_entry_id;

+#[cfg(feature = "op_delete_message")]
 pub(crate) mod shape_invalid_id_format;

+#[cfg(feature = "op_send_message")]
 pub(crate) mod shape_invalid_message_contents;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_invalid_security;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_access_denied;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_disabled;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_invalid_key_usage;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_invalid_state;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_not_found;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_opt_in_required;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_throttled;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) mod shape_list_dead_letter_source_queues_input;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks_input;

+#[cfg(feature = "op_list_queue_tags")]
 pub(crate) mod shape_list_queue_tags_input;

+#[cfg(feature = "op_list_queues")]
 pub(crate) mod shape_list_queues_input;

+#[cfg(feature = "op_change_message_visibility")]
 pub(crate) mod shape_message_not_inflight;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub(crate) mod shape_over_limit;

+#[cfg(feature = "op_purge_queue")]
 pub(crate) mod shape_purge_queue_in_progress;

+#[cfg(feature = "op_purge_queue")]
 pub(crate) mod shape_purge_queue_input;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_queue_deleted_recently;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_queue_does_not_exist;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_queue_name_exists;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 pub(crate) mod shape_receipt_handle_is_invalid;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_receive_message_input;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_request_throttled;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_input;

+#[cfg(feature = "op_send_message")]
 pub(crate) mod shape_send_message_input;

+#[cfg(feature = "op_set_queue_attributes")]
 pub(crate) mod shape_set_queue_attributes_input;

+#[cfg(feature = "op_start_message_move_task")]
 pub(crate) mod shape_start_message_move_task_input;

+#[cfg(feature = "op_tag_queue")]
 pub(crate) mod shape_tag_queue_input;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_too_many_entries_in_batch_request;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_unsupported_operation;

+#[cfg(feature = "op_untag_queue")]
 pub(crate) mod shape_untag_queue_input;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_batch_result_error_entry_list;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_request_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_result_entry_list;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_request_entry;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_result_entry_list;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks_result_entry_list;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_message_attribute_value;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message_list;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub(crate) mod shape_message_system_attribute_value;

+#[cfg(feature = "op_get_queue_attributes")]
 pub(crate) mod shape_queue_attribute_map;

+#[cfg(any(feature = "op_list_dead_letter_source_queues", feature = "op_list_queues"))]
 pub(crate) mod shape_queue_url_list;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_request_entry;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_result_entry_list;

+#[cfg(feature = "op_list_queue_tags")]
 pub(crate) mod shape_tag_map;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_batch_result_error_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_result_entry;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_result_entry;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks_result_entry;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_result_entry;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message_body_attribute_map;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message_system_attribute_map;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_binary_list;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_string_list;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) fn change_message_visibility_batch_output_output_correct_errors(
     mut builder: crate::operation::change_message_visibility_batch::builders::ChangeMessageVisibilityBatchOutputBuilder,
 ) -> crate::operation::change_message_visibility_batch::builders::ChangeMessageVisibilityBatchOutputBuilder {
@@ -11,6 +12,7 @@
     builder
 }

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) fn delete_message_batch_output_output_correct_errors(
     mut builder: crate::operation::delete_message_batch::builders::DeleteMessageBatchOutputBuilder,
 ) -> crate::operation::delete_message_batch::builders::DeleteMessageBatchOutputBuilder {
@@ -23,6 +25,7 @@
     builder
 }

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) fn list_dead_letter_source_queues_output_output_correct_errors(
     mut builder: crate::operation::list_dead_letter_source_queues::builders::ListDeadLetterSourceQueuesOutputBuilder,
 ) -> crate::operation::list_dead_letter_source_queues::builders::ListDeadLetterSourceQueuesOutputBuilder {
@@ -32,6 +35,7 @@
     builder
 }

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) fn send_message_batch_output_output_correct_errors(
     mut builder: crate::operation::send_message_batch::builders::SendMessageBatchOutputBuilder,
 ) -> crate::operation::send_message_batch::builders::SendMessageBatchOutputBuilder {
@@ -44,6 +48,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) fn batch_result_error_entry_correct_errors(
     mut builder: crate::types::builders::BatchResultErrorEntryBuilder,
 ) -> crate::types::builders::BatchResultErrorEntryBuilder {
@@ -59,6 +68,7 @@
     builder
 }

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) fn change_message_visibility_batch_result_entry_correct_errors(
     mut builder: crate::types::builders::ChangeMessageVisibilityBatchResultEntryBuilder,
 ) -> crate::types::builders::ChangeMessageVisibilityBatchResultEntryBuilder {
@@ -68,6 +78,7 @@
     builder
 }

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) fn delete_message_batch_result_entry_correct_errors(
     mut builder: crate::types::builders::DeleteMessageBatchResultEntryBuilder,
 ) -> crate::types::builders::DeleteMessageBatchResultEntryBuilder {
@@ -77,6 +88,7 @@
     builder
 }

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) fn send_message_batch_result_entry_correct_errors(
     mut builder: crate::types::builders::SendMessageBatchResultEntryBuilder,
 ) -> crate::types::builders::SendMessageBatchResultEntryBuilder {
@@ -92,6 +104,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) fn message_attribute_value_correct_errors(
     mut builder: crate::types::builders::MessageAttributeValueBuilder,
 ) -> crate::types::builders::MessageAttributeValueBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,58 +1,112 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_request_entry::ChangeMessageVisibilityBatchRequestEntry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_result_entry::ChangeMessageVisibilityBatchResultEntry;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntry;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::_queue_attribute_name::QueueAttributeName;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_request_entry::DeleteMessageBatchRequestEntry;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_result_entry::DeleteMessageBatchResultEntry;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub use crate::types::_list_message_move_tasks_result_entry::ListMessageMoveTasksResultEntry;

+#[cfg(feature = "op_receive_message")]
 pub use crate::types::_message_system_attribute_name::MessageSystemAttributeName;

+#[cfg(feature = "op_receive_message")]
 pub use crate::types::_message::Message;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_message_attribute_value::MessageAttributeValue;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub use crate::types::_message_system_attribute_name_for_sends::MessageSystemAttributeNameForSends;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub use crate::types::_message_system_attribute_value::MessageSystemAttributeValue;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_request_entry::SendMessageBatchRequestEntry;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_result_entry::SendMessageBatchResultEntry;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _batch_result_error_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 mod _change_message_visibility_batch_request_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 mod _change_message_visibility_batch_result_entry;

+#[cfg(feature = "op_delete_message_batch")]
 mod _delete_message_batch_request_entry;

+#[cfg(feature = "op_delete_message_batch")]
 mod _delete_message_batch_result_entry;

+#[cfg(feature = "op_list_message_move_tasks")]
 mod _list_message_move_tasks_result_entry;

+#[cfg(feature = "op_receive_message")]
 mod _message;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _message_attribute_value;

+#[cfg(feature = "op_receive_message")]
 mod _message_system_attribute_name;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 mod _message_system_attribute_name_for_sends;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 mod _message_system_attribute_value;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 mod _queue_attribute_name;

+#[cfg(feature = "op_send_message_batch")]
 mod _send_message_batch_request_entry;

+#[cfg(feature = "op_send_message_batch")]
 mod _send_message_batch_result_entry;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,22 +1,41 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_request_entry::ChangeMessageVisibilityBatchRequestEntryBuilder;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_result_entry::ChangeMessageVisibilityBatchResultEntryBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntryBuilder;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_request_entry::DeleteMessageBatchRequestEntryBuilder;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_result_entry::DeleteMessageBatchResultEntryBuilder;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub use crate::types::_list_message_move_tasks_result_entry::ListMessageMoveTasksResultEntryBuilder;

+#[cfg(feature = "op_receive_message")]
 pub use crate::types::_message::MessageBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_message_attribute_value::MessageAttributeValueBuilder;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub use crate::types::_message_system_attribute_value::MessageSystemAttributeValueBuilder;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_request_entry::SendMessageBatchRequestEntryBuilder;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_result_entry::SendMessageBatchResultEntryBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,114 +1,512 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_address::InvalidAddress;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_security::InvalidSecurity;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_over_limit::OverLimit;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_queue_does_not_exist::QueueDoesNotExist;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_request_throttled::RequestThrottled;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_unsupported_operation::UnsupportedOperation;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(feature = "op_change_message_visibility")]
 pub use crate::types::error::_message_not_inflight::MessageNotInflight;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 pub use crate::types::error::_receipt_handle_is_invalid::ReceiptHandleIsInvalid;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_batch_entry_ids_not_distinct::BatchEntryIdsNotDistinct;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_empty_batch_request::EmptyBatchRequest;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_invalid_batch_entry_id::InvalidBatchEntryId;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_too_many_entries_in_batch_request::TooManyEntriesInBatchRequest;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_invalid_attribute_name::InvalidAttributeName;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 pub use crate::types::error::_invalid_attribute_value::InvalidAttributeValue;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_deleted_recently::QueueDeletedRecently;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_name_exists::QueueNameExists;

+#[cfg(feature = "op_delete_message")]
 pub use crate::types::error::_invalid_id_format::InvalidIdFormat;

+#[cfg(feature = "op_purge_queue")]
 pub use crate::types::error::_purge_queue_in_progress::PurgeQueueInProgress;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_access_denied::KmsAccessDenied;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_disabled::KmsDisabled;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_key_usage::KmsInvalidKeyUsage;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_state::KmsInvalidState;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_not_found::KmsNotFound;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequired;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_throttled::KmsThrottled;

+#[cfg(feature = "op_send_message")]
 pub use crate::types::error::_invalid_message_contents::InvalidMessageContents;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::error::_batch_request_too_long::BatchRequestTooLong;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _batch_entry_ids_not_distinct;

+#[cfg(feature = "op_send_message_batch")]
 mod _batch_request_too_long;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _empty_batch_request;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _invalid_address;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 mod _invalid_attribute_name;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 mod _invalid_attribute_value;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _invalid_batch_entry_id;

+#[cfg(feature = "op_delete_message")]
 mod _invalid_id_format;

+#[cfg(feature = "op_send_message")]
 mod _invalid_message_contents;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _invalid_security;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_access_denied;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_disabled;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_invalid_key_usage;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_invalid_state;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_not_found;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_opt_in_required;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_throttled;

+#[cfg(feature = "op_change_message_visibility")]
 mod _message_not_inflight;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 mod _over_limit;

+#[cfg(feature = "op_purge_queue")]
 mod _purge_queue_in_progress;

+#[cfg(feature = "op_create_queue")]
 mod _queue_deleted_recently;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _queue_does_not_exist;

+#[cfg(feature = "op_create_queue")]
 mod _queue_name_exists;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 mod _receipt_handle_is_invalid;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _request_throttled;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _too_many_entries_in_batch_request;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _unsupported_operation;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,56 +1,255 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_address::InvalidAddressBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_security::InvalidSecurityBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_over_limit::OverLimitBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_queue_does_not_exist::QueueDoesNotExistBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_request_throttled::RequestThrottledBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_unsupported_operation::UnsupportedOperationBuilder;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(feature = "op_change_message_visibility")]
 pub use crate::types::error::_message_not_inflight::MessageNotInflightBuilder;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 pub use crate::types::error::_receipt_handle_is_invalid::ReceiptHandleIsInvalidBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_batch_entry_ids_not_distinct::BatchEntryIdsNotDistinctBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_empty_batch_request::EmptyBatchRequestBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_invalid_batch_entry_id::InvalidBatchEntryIdBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_too_many_entries_in_batch_request::TooManyEntriesInBatchRequestBuilder;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_invalid_attribute_name::InvalidAttributeNameBuilder;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 pub use crate::types::error::_invalid_attribute_value::InvalidAttributeValueBuilder;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_deleted_recently::QueueDeletedRecentlyBuilder;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_name_exists::QueueNameExistsBuilder;

+#[cfg(feature = "op_delete_message")]
 pub use crate::types::error::_invalid_id_format::InvalidIdFormatBuilder;

+#[cfg(feature = "op_purge_queue")]
 pub use crate::types::error::_purge_queue_in_progress::PurgeQueueInProgressBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_access_denied::KmsAccessDeniedBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_disabled::KmsDisabledBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_key_usage::KmsInvalidKeyUsageBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_state::KmsInvalidStateBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_not_found::KmsNotFoundBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequiredBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_throttled::KmsThrottledBuilder;

+#[cfg(feature = "op_send_message")]
 pub use crate::types::error::_invalid_message_contents::InvalidMessageContentsBuilder;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::error::_batch_request_too_long::BatchRequestTooLongBuilder;
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

@@ -153,6 +133,29 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_add_permission = []
+op_cancel_message_move_task = []
+op_change_message_visibility = []
+op_change_message_visibility_batch = []
+op_create_queue = []
+op_delete_message = []
+op_delete_message_batch = []
+op_delete_queue = []
+op_get_queue_attributes = []
+op_get_queue_url = []
+op_list_dead_letter_source_queues = []
+op_list_message_move_tasks = []
+op_list_queues = []
+op_list_queue_tags = []
+op_purge_queue = []
+op_receive_message = []
+op_remove_permission = []
+op_send_message = []
+op_send_message_batch = []
+op_set_queue_attributes = []
+op_start_message_move_task = []
+op_tag_queue = []
+op_untag_queue = []

 [hints]
 mostly-unused = true
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,14 +136,19 @@
     }
 }

+#[cfg(feature = "op_add_permission")]
 mod add_permission;

+#[cfg(feature = "op_cancel_message_move_task")]
 mod cancel_message_move_task;

+#[cfg(feature = "op_change_message_visibility")]
 mod change_message_visibility;

+#[cfg(feature = "op_change_message_visibility_batch")]
 mod change_message_visibility_batch;

+#[cfg(feature = "op_create_queue")]
 mod create_queue;

 /// Operation customization and supporting types.
@@ -173,38 +178,56 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_message")]
 mod delete_message;

+#[cfg(feature = "op_delete_message_batch")]
 mod delete_message_batch;

+#[cfg(feature = "op_delete_queue")]
 mod delete_queue;

+#[cfg(feature = "op_get_queue_attributes")]
 mod get_queue_attributes;

+#[cfg(feature = "op_get_queue_url")]
 mod get_queue_url;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 mod list_dead_letter_source_queues;

+#[cfg(feature = "op_list_message_move_tasks")]
 mod list_message_move_tasks;

+#[cfg(feature = "op_list_queue_tags")]
 mod list_queue_tags;

+#[cfg(feature = "op_list_queues")]
 mod list_queues;

+#[cfg(feature = "op_purge_queue")]
 mod purge_queue;

+#[cfg(feature = "op_receive_message")]
 mod receive_message;

+#[cfg(feature = "op_remove_permission")]
 mod remove_permission;

+#[cfg(feature = "op_send_message")]
 mod send_message;

+#[cfg(feature = "op_send_message_batch")]
 mod send_message_batch;

+#[cfg(feature = "op_set_queue_attributes")]
 mod set_queue_attributes;

+#[cfg(feature = "op_start_message_move_task")]
 mod start_message_move_task;

+#[cfg(feature = "op_tag_queue")]
 mod tag_queue;

+#[cfg(feature = "op_untag_queue")]
 mod untag_queue;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,31 +3,120 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>Two or more batch entries in the request have the same <code>Id</code>.</p>
     BatchEntryIdsNotDistinct(crate::types::error::BatchEntryIdsNotDistinct),
+    #[cfg(feature = "op_send_message_batch")]
     /// <p>The length of all the messages put together is more than the limit.</p>
     BatchRequestTooLong(crate::types::error::BatchRequestTooLong),
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The batch request doesn't contain any entries.</p>
     EmptyBatchRequest(crate::types::error::EmptyBatchRequest),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>The specified ID is invalid.</p>
     InvalidAddress(crate::types::error::InvalidAddress),
+    #[cfg(any(
+        feature = "op_create_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_set_queue_attributes"
+    ))]
     /// <p>The specified attribute doesn't exist.</p>
     InvalidAttributeName(crate::types::error::InvalidAttributeName),
+    #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
     /// <p>A queue attribute value is invalid.</p>
     InvalidAttributeValue(crate::types::error::InvalidAttributeValue),
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The <code>Id</code> of a batch entry in a batch request doesn't abide by the specification.</p>
     InvalidBatchEntryId(crate::types::error::InvalidBatchEntryId),
+    #[cfg(feature = "op_delete_message")]
     /// <p>The specified receipt handle isn't valid for the current version.</p>
     #[deprecated(note = "exception has been included in ReceiptHandleIsInvalid")]
     InvalidIdFormat(crate::types::error::InvalidIdFormat),
+    #[cfg(feature = "op_send_message")]
     /// <p>The message contains characters outside the allowed set.</p>
     InvalidMessageContents(crate::types::error::InvalidMessageContents),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>The request was not made over HTTPS or did not use SigV4 for signing.</p>
     InvalidSecurity(crate::types::error::InvalidSecurity),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The caller doesn't have the required KMS access.</p>
     KmsAccessDenied(crate::types::error::KmsAccessDenied),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was denied due to request throttling.</p>
     KmsDisabled(crate::types::error::KmsDisabled),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected for one of the following reasons:</p>
     /// <ul>
     /// <li>
@@ -36,28 +125,103 @@
     /// <p>The encryption algorithm or signing algorithm specified for the operation is incompatible with the type of key material in the KMS key (KeySpec).</p></li>
     /// </ul>
     KmsInvalidKeyUsage(crate::types::error::KmsInvalidKeyUsage),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected because the state of the specified resource is not valid for this request.</p>
     KmsInvalidState(crate::types::error::KmsInvalidState),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected because the specified entity or resource could not be found.</p>
     KmsNotFound(crate::types::error::KmsNotFound),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The request was rejected because the specified key policy isn't syntactically or semantically correct.</p>
     KmsOptInRequired(crate::types::error::KmsOptInRequired),
+    #[cfg(any(
+        feature = "op_receive_message",
+        feature = "op_send_message",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>Amazon Web Services KMS throttles requests for the following conditions.</p>
     KmsThrottled(crate::types::error::KmsThrottled),
+    #[cfg(feature = "op_change_message_visibility")]
     /// <p>The specified message isn't in flight.</p>
     MessageNotInflight(crate::types::error::MessageNotInflight),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_receive_message",
+        feature = "op_set_queue_attributes"
+    ))]
     /// <p>The specified action violates a limit. For example, <code>ReceiveMessage</code> returns this error if the maximum number of in flight messages is reached and <code>AddPermission</code> returns this error if the maximum number of permissions for the queue is reached.</p>
     OverLimit(crate::types::error::OverLimit),
+    #[cfg(feature = "op_purge_queue")]
     /// <p>Indicates that the specified queue previously received a <code>PurgeQueue</code> request within the last 60 seconds (the time it can take to delete the messages in the queue).</p>
     PurgeQueueInProgress(crate::types::error::PurgeQueueInProgress),
+    #[cfg(feature = "op_create_queue")]
     /// <p>You must wait 60 seconds after deleting a queue before you can create another queue with the same name.</p>
     QueueDeletedRecently(crate::types::error::QueueDeletedRecently),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_queue_tags",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>Ensure that the <code>QueueUrl</code> is correct and that the queue has not been deleted.</p>
     QueueDoesNotExist(crate::types::error::QueueDoesNotExist),
+    #[cfg(feature = "op_create_queue")]
     /// <p>A queue with this name already exists. Amazon SQS returns this error only if the request includes attributes whose values differ from those of the existing queue.</p>
     QueueNameExists(crate::types::error::QueueNameExists),
+    #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
     /// <p>The specified receipt handle isn't valid.</p>
     ReceiptHandleIsInvalid(crate::types::error::ReceiptHandleIsInvalid),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>The request was denied due to request throttling.</p>
     /// <ul>
     /// <li>
@@ -66,10 +230,45 @@
     /// <p>Ensure that the request rate is within the Amazon SQS limits for sending messages. For more information, see <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-quotas.html#quotas-requests">Amazon SQS quotas</a> in the <i>Amazon SQS Developer Guide</i>.</p></li>
     /// </ul>
     RequestThrottled(crate::types::error::RequestThrottled),
+    #[cfg(any(
+        feature = "op_cancel_message_move_task",
+        feature = "op_list_message_move_tasks",
+        feature = "op_start_message_move_task"
+    ))]
     /// <p>One or more specified resources don't exist.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_change_message_visibility_batch",
+        feature = "op_delete_message_batch",
+        feature = "op_send_message_batch"
+    ))]
     /// <p>The batch request contains more entries than permissible. For Amazon SQS, the maximum number of entries you can include in a single <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SendMessageBatch.html">SendMessageBatch</a>, <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_DeleteMessageBatch.html">DeleteMessageBatch</a>, or <a href="https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_ChangeMessageVisibilityBatch.html">ChangeMessageVisibilityBatch</a> request is 10.</p>
     TooManyEntriesInBatchRequest(crate::types::error::TooManyEntriesInBatchRequest),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_cancel_message_move_task",
+        feature = "op_change_message_visibility",
+        feature = "op_change_message_visibility_batch",
+        feature = "op_create_queue",
+        feature = "op_delete_message",
+        feature = "op_delete_message_batch",
+        feature = "op_delete_queue",
+        feature = "op_get_queue_attributes",
+        feature = "op_get_queue_url",
+        feature = "op_list_dead_letter_source_queues",
+        feature = "op_list_message_move_tasks",
+        feature = "op_list_queue_tags",
+        feature = "op_list_queues",
+        feature = "op_purge_queue",
+        feature = "op_receive_message",
+        feature = "op_remove_permission",
+        feature = "op_send_message",
+        feature = "op_send_message_batch",
+        feature = "op_set_queue_attributes",
+        feature = "op_start_message_move_task",
+        feature = "op_tag_queue",
+        feature = "op_untag_queue"
+    ))]
     /// <p>Error code 400. Unsupported operation.</p>
     UnsupportedOperation(crate::types::error::UnsupportedOperation),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -86,33 +285,232 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::BatchEntryIdsNotDistinct(inner) => inner.fmt(f),
+            #[cfg(feature = "op_send_message_batch")]
             Error::BatchRequestTooLong(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::EmptyBatchRequest(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidAddress(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::InvalidAttributeName(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Error::InvalidAttributeValue(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::InvalidBatchEntryId(inner) => inner.fmt(f),
+            #[cfg(feature = "op_delete_message")]
             Error::InvalidIdFormat(inner) => inner.fmt(f),
+            #[cfg(feature = "op_send_message")]
             Error::InvalidMessageContents(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidSecurity(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsAccessDenied(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsDisabled(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidKeyUsage(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidState(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsNotFound(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsOptInRequired(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsThrottled(inner) => inner.fmt(f),
+            #[cfg(feature = "op_change_message_visibility")]
             Error::MessageNotInflight(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::OverLimit(inner) => inner.fmt(f),
+            #[cfg(feature = "op_purge_queue")]
             Error::PurgeQueueInProgress(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueDeletedRecently(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::QueueDoesNotExist(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueNameExists(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Error::ReceiptHandleIsInvalid(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::RequestThrottled(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::TooManyEntriesInBatchRequest(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::UnsupportedOperation(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -137,38 +535,238 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::BatchEntryIdsNotDistinct(inner) => inner.meta(),
+            #[cfg(feature = "op_send_message_batch")]
             Self::BatchRequestTooLong(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::EmptyBatchRequest(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidAddress(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::InvalidAttributeName(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Self::InvalidAttributeValue(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::InvalidBatchEntryId(inner) => inner.meta(),
+            #[cfg(feature = "op_delete_message")]
             Self::InvalidIdFormat(inner) => inner.meta(),
+            #[cfg(feature = "op_send_message")]
             Self::InvalidMessageContents(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidSecurity(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsAccessDenied(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsDisabled(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidKeyUsage(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidState(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsNotFound(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsOptInRequired(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsThrottled(inner) => inner.meta(),
+            #[cfg(feature = "op_change_message_visibility")]
             Self::MessageNotInflight(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::OverLimit(inner) => inner.meta(),
+            #[cfg(feature = "op_purge_queue")]
             Self::PurgeQueueInProgress(inner) => inner.meta(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueDeletedRecently(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::QueueDoesNotExist(inner) => inner.meta(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueNameExists(inner) => inner.meta(),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Self::ReceiptHandleIsInvalid(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::RequestThrottled(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::TooManyEntriesInBatchRequest(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::UnsupportedOperation(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::add_permission::AddPermissionError, R>>
     for Error
@@ -190,6 +788,7 @@
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl From<crate::operation::add_permission::AddPermissionError> for Error {
     fn from(err: crate::operation::add_permission::AddPermissionError) -> Self {
         match err {
@@ -211,6 +810,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_message_move_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -236,6 +836,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_message_move_task")]
 impl From<crate::operation::cancel_message_move_task::CancelMessageMoveTaskError> for Error {
     fn from(err: crate::operation::cancel_message_move_task::CancelMessageMoveTaskError) -> Self {
         match err {
@@ -260,6 +861,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -285,6 +887,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility")]
 impl From<crate::operation::change_message_visibility::ChangeMessageVisibilityError> for Error {
     fn from(err: crate::operation::change_message_visibility::ChangeMessageVisibilityError) -> Self {
         match err {
@@ -315,6 +918,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility_batch")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -340,6 +944,7 @@
         }
     }
 }
+#[cfg(feature = "op_change_message_visibility_batch")]
 impl From<crate::operation::change_message_visibility_batch::ChangeMessageVisibilityBatchError> for Error {
     fn from(err: crate::operation::change_message_visibility_batch::ChangeMessageVisibilityBatchError) -> Self {
         match err {
@@ -374,6 +979,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_queue::CreateQueueError, R>>
     for Error
 where
@@ -391,6 +997,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_queue")]
 impl From<crate::operation::create_queue::CreateQueueError> for Error {
     fn from(err: crate::operation::create_queue::CreateQueueError) -> Self {
         match err {
@@ -414,6 +1021,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_message::DeleteMessageError, R>>
     for Error
@@ -435,6 +1043,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message")]
 impl From<crate::operation::delete_message::DeleteMessageError> for Error {
     fn from(err: crate::operation::delete_message::DeleteMessageError) -> Self {
         match err {
@@ -461,6 +1070,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message_batch")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -486,6 +1096,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_message_batch")]
 impl From<crate::operation::delete_message_batch::DeleteMessageBatchError> for Error {
     fn from(err: crate::operation::delete_message_batch::DeleteMessageBatchError) -> Self {
         match err {
@@ -522,6 +1133,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_queue::DeleteQueueError, R>>
     for Error
 where
@@ -539,6 +1151,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_queue")]
 impl From<crate::operation::delete_queue::DeleteQueueError> for Error {
     fn from(err: crate::operation::delete_queue::DeleteQueueError) -> Self {
         match err {
@@ -555,6 +1168,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -580,6 +1194,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_attributes")]
 impl From<crate::operation::get_queue_attributes::GetQueueAttributesError> for Error {
     fn from(err: crate::operation::get_queue_attributes::GetQueueAttributesError) -> Self {
         match err {
@@ -607,6 +1222,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_url")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_queue_url::GetQueueUrlError, R>>
     for Error
 where
@@ -624,6 +1240,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_queue_url")]
 impl From<crate::operation::get_queue_url::GetQueueUrlError> for Error {
     fn from(err: crate::operation::get_queue_url::GetQueueUrlError) -> Self {
         match err {
@@ -642,6 +1259,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dead_letter_source_queues")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -667,6 +1285,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dead_letter_source_queues")]
 impl From<crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesError> for Error {
     fn from(err: crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesError) -> Self {
         match err {
@@ -691,6 +1310,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_message_move_tasks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -716,6 +1336,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_message_move_tasks")]
 impl From<crate::operation::list_message_move_tasks::ListMessageMoveTasksError> for Error {
     fn from(err: crate::operation::list_message_move_tasks::ListMessageMoveTasksError) -> Self {
         match err {
@@ -740,6 +1361,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queues")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_queues::ListQueuesError, R>>
     for Error
 where
@@ -757,6 +1379,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queues")]
 impl From<crate::operation::list_queues::ListQueuesError> for Error {
     fn from(err: crate::operation::list_queues::ListQueuesError) -> Self {
         match err {
@@ -770,6 +1393,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queue_tags")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_queue_tags::ListQueueTagsError, R>>
     for Error
@@ -791,6 +1415,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_queue_tags")]
 impl From<crate::operation::list_queue_tags::ListQueueTagsError> for Error {
     fn from(err: crate::operation::list_queue_tags::ListQueueTagsError) -> Self {
         match err {
@@ -813,6 +1438,7 @@
         }
     }
 }
+#[cfg(feature = "op_purge_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::purge_queue::PurgeQueueError, R>>
     for Error
 where
@@ -830,6 +1456,7 @@
         }
     }
 }
+#[cfg(feature = "op_purge_queue")]
 impl From<crate::operation::purge_queue::PurgeQueueError> for Error {
     fn from(err: crate::operation::purge_queue::PurgeQueueError) -> Self {
         match err {
@@ -847,6 +1474,7 @@
         }
     }
 }
+#[cfg(feature = "op_receive_message")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::receive_message::ReceiveMessageError, R>>
     for Error
@@ -868,6 +1496,7 @@
         }
     }
 }
+#[cfg(feature = "op_receive_message")]
 impl From<crate::operation::receive_message::ReceiveMessageError> for Error {
     fn from(err: crate::operation::receive_message::ReceiveMessageError) -> Self {
         match err {
@@ -906,6 +1535,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -931,6 +1561,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl From<crate::operation::remove_permission::RemovePermissionError> for Error {
     fn from(err: crate::operation::remove_permission::RemovePermissionError) -> Self {
         match err {
@@ -953,6 +1584,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::send_message::SendMessageError, R>>
     for Error
 where
@@ -970,6 +1602,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message")]
 impl From<crate::operation::send_message::SendMessageError> for Error {
     fn from(err: crate::operation::send_message::SendMessageError) -> Self {
         match err {
@@ -998,6 +1631,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message_batch")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1023,6 +1657,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_message_batch")]
 impl From<crate::operation::send_message_batch::SendMessageBatchError> for Error {
     fn from(err: crate::operation::send_message_batch::SendMessageBatchError) -> Self {
         match err {
@@ -1081,6 +1716,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_queue_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1106,6 +1742,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_queue_attributes")]
 impl From<crate::operation::set_queue_attributes::SetQueueAttributesError> for Error {
     fn from(err: crate::operation::set_queue_attributes::SetQueueAttributesError) -> Self {
         match err {
@@ -1139,6 +1776,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_message_move_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1164,6 +1802,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_message_move_task")]
 impl From<crate::operation::start_message_move_task::StartMessageMoveTaskError> for Error {
     fn from(err: crate::operation::start_message_move_task::StartMessageMoveTaskError) -> Self {
         match err {
@@ -1188,6 +1827,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_queue::TagQueueError, R>>
     for Error
 where
@@ -1205,6 +1845,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_queue")]
 impl From<crate::operation::tag_queue::TagQueueError> for Error {
     fn from(err: crate::operation::tag_queue::TagQueueError) -> Self {
         match err {
@@ -1219,6 +1860,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_queue")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_queue::UntagQueueError, R>>
     for Error
 where
@@ -1236,6 +1878,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_queue")]
 impl From<crate::operation::untag_queue::UntagQueueError> for Error {
     fn from(err: crate::operation::untag_queue::UntagQueueError) -> Self {
         match err {
@@ -1253,33 +1896,232 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::BatchEntryIdsNotDistinct(inner) => inner.source(),
+            #[cfg(feature = "op_send_message_batch")]
             Error::BatchRequestTooLong(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::EmptyBatchRequest(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidAddress(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::InvalidAttributeName(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Error::InvalidAttributeValue(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::InvalidBatchEntryId(inner) => inner.source(),
+            #[cfg(feature = "op_delete_message")]
             Error::InvalidIdFormat(inner) => inner.source(),
+            #[cfg(feature = "op_send_message")]
             Error::InvalidMessageContents(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::InvalidSecurity(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsAccessDenied(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsDisabled(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidKeyUsage(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsInvalidState(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsNotFound(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsOptInRequired(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Error::KmsThrottled(inner) => inner.source(),
+            #[cfg(feature = "op_change_message_visibility")]
             Error::MessageNotInflight(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Error::OverLimit(inner) => inner.source(),
+            #[cfg(feature = "op_purge_queue")]
             Error::PurgeQueueInProgress(inner) => inner.source(),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueDeletedRecently(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::QueueDoesNotExist(inner) => inner.source(),
+            #[cfg(feature = "op_create_queue")]
             Error::QueueNameExists(inner) => inner.source(),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Error::ReceiptHandleIsInvalid(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::RequestThrottled(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Error::TooManyEntriesInBatchRequest(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Error::UnsupportedOperation(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -1288,33 +2130,232 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::BatchEntryIdsNotDistinct(e) => e.request_id(),
+            #[cfg(feature = "op_send_message_batch")]
             Self::BatchRequestTooLong(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::EmptyBatchRequest(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidAddress(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::InvalidAttributeName(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
             Self::InvalidAttributeValue(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::InvalidBatchEntryId(e) => e.request_id(),
+            #[cfg(feature = "op_delete_message")]
             Self::InvalidIdFormat(e) => e.request_id(),
+            #[cfg(feature = "op_send_message")]
             Self::InvalidMessageContents(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::InvalidSecurity(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsAccessDenied(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsDisabled(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidKeyUsage(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsInvalidState(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsNotFound(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsOptInRequired(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_receive_message",
+                feature = "op_send_message",
+                feature = "op_send_message_batch"
+            ))]
             Self::KmsThrottled(e) => e.request_id(),
+            #[cfg(feature = "op_change_message_visibility")]
             Self::MessageNotInflight(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_receive_message",
+                feature = "op_set_queue_attributes"
+            ))]
             Self::OverLimit(e) => e.request_id(),
+            #[cfg(feature = "op_purge_queue")]
             Self::PurgeQueueInProgress(e) => e.request_id(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueDeletedRecently(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_queue_tags",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::QueueDoesNotExist(e) => e.request_id(),
+            #[cfg(feature = "op_create_queue")]
             Self::QueueNameExists(e) => e.request_id(),
+            #[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
             Self::ReceiptHandleIsInvalid(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::RequestThrottled(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_message_move_task",
+                feature = "op_list_message_move_tasks",
+                feature = "op_start_message_move_task"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_change_message_visibility_batch",
+                feature = "op_delete_message_batch",
+                feature = "op_send_message_batch"
+            ))]
             Self::TooManyEntriesInBatchRequest(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_cancel_message_move_task",
+                feature = "op_change_message_visibility",
+                feature = "op_change_message_visibility_batch",
+                feature = "op_create_queue",
+                feature = "op_delete_message",
+                feature = "op_delete_message_batch",
+                feature = "op_delete_queue",
+                feature = "op_get_queue_attributes",
+                feature = "op_get_queue_url",
+                feature = "op_list_dead_letter_source_queues",
+                feature = "op_list_message_move_tasks",
+                feature = "op_list_queue_tags",
+                feature = "op_list_queues",
+                feature = "op_purge_queue",
+                feature = "op_receive_message",
+                feature = "op_remove_permission",
+                feature = "op_send_message",
+                feature = "op_send_message_batch",
+                feature = "op_set_queue_attributes",
+                feature = "op_start_message_move_task",
+                feature = "op_tag_queue",
+                feature = "op_untag_queue"
+            ))]
             Self::UnsupportedOperation(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) fn reflens_list_dead_letter_source_queues_output_output_next_token(
     input: &crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_queues")]
 pub(crate) fn reflens_list_queues_output_output_next_token(
     input: &crate::operation::list_queues::ListQueuesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) fn lens_list_dead_letter_source_queues_output_output_queue_urls(
     input: crate::operation::list_dead_letter_source_queues::ListDeadLetterSourceQueuesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -26,6 +29,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_queues")]
 pub(crate) fn lens_list_queues_output_output_queue_urls(
     input: crate::operation::list_queues::ListQueuesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,71 +1,94 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_add_permission")]
 /// Types for the `AddPermission` operation.
 pub mod add_permission;

+#[cfg(feature = "op_cancel_message_move_task")]
 /// Types for the `CancelMessageMoveTask` operation.
 pub mod cancel_message_move_task;

+#[cfg(feature = "op_change_message_visibility")]
 /// Types for the `ChangeMessageVisibility` operation.
 pub mod change_message_visibility;

+#[cfg(feature = "op_change_message_visibility_batch")]
 /// Types for the `ChangeMessageVisibilityBatch` operation.
 pub mod change_message_visibility_batch;

+#[cfg(feature = "op_create_queue")]
 /// Types for the `CreateQueue` operation.
 pub mod create_queue;

+#[cfg(feature = "op_delete_message")]
 /// Types for the `DeleteMessage` operation.
 pub mod delete_message;

+#[cfg(feature = "op_delete_message_batch")]
 /// Types for the `DeleteMessageBatch` operation.
 pub mod delete_message_batch;

+#[cfg(feature = "op_delete_queue")]
 /// Types for the `DeleteQueue` operation.
 pub mod delete_queue;

+#[cfg(feature = "op_get_queue_attributes")]
 /// Types for the `GetQueueAttributes` operation.
 pub mod get_queue_attributes;

+#[cfg(feature = "op_get_queue_url")]
 /// Types for the `GetQueueUrl` operation.
 pub mod get_queue_url;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 /// Types for the `ListDeadLetterSourceQueues` operation.
 pub mod list_dead_letter_source_queues;

+#[cfg(feature = "op_list_message_move_tasks")]
 /// Types for the `ListMessageMoveTasks` operation.
 pub mod list_message_move_tasks;

+#[cfg(feature = "op_list_queue_tags")]
 /// Types for the `ListQueueTags` operation.
 pub mod list_queue_tags;

+#[cfg(feature = "op_list_queues")]
 /// Types for the `ListQueues` operation.
 pub mod list_queues;

+#[cfg(feature = "op_purge_queue")]
 /// Types for the `PurgeQueue` operation.
 pub mod purge_queue;

+#[cfg(feature = "op_receive_message")]
 /// Types for the `ReceiveMessage` operation.
 pub mod receive_message;

+#[cfg(feature = "op_remove_permission")]
 /// Types for the `RemovePermission` operation.
 pub mod remove_permission;

+#[cfg(feature = "op_send_message")]
 /// Types for the `SendMessage` operation.
 pub mod send_message;

+#[cfg(feature = "op_send_message_batch")]
 /// Types for the `SendMessageBatch` operation.
 pub mod send_message_batch;

+#[cfg(feature = "op_set_queue_attributes")]
 /// Types for the `SetQueueAttributes` operation.
 pub mod set_queue_attributes;

+#[cfg(feature = "op_start_message_move_task")]
 /// Types for the `StartMessageMoveTask` operation.
 pub mod start_message_move_task;

+#[cfg(feature = "op_tag_queue")]
 /// Types for the `TagQueue` operation.
 pub mod tag_queue;

+#[cfg(feature = "op_untag_queue")]
 /// Types for the `UntagQueue` operation.
 pub mod untag_queue;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,29 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +42,31 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -35,54 +85,103 @@
     Ok(builder)
 }

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission;

+#[cfg(feature = "op_cancel_message_move_task")]
 pub(crate) mod shape_cancel_message_move_task;

+#[cfg(feature = "op_change_message_visibility")]
 pub(crate) mod shape_change_message_visibility;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_create_queue;

+#[cfg(feature = "op_delete_message")]
 pub(crate) mod shape_delete_message;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch;

+#[cfg(feature = "op_delete_queue")]
 pub(crate) mod shape_delete_queue;

+#[cfg(feature = "op_get_queue_attributes")]
 pub(crate) mod shape_get_queue_attributes;

+#[cfg(feature = "op_get_queue_url")]
 pub(crate) mod shape_get_queue_url;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) mod shape_list_dead_letter_source_queues;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks;

+#[cfg(feature = "op_list_queue_tags")]
 pub(crate) mod shape_list_queue_tags;

+#[cfg(feature = "op_list_queues")]
 pub(crate) mod shape_list_queues;

+#[cfg(feature = "op_purge_queue")]
 pub(crate) mod shape_purge_queue;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_receive_message;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission;

+#[cfg(feature = "op_send_message")]
 pub(crate) mod shape_send_message;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch;

+#[cfg(feature = "op_set_queue_attributes")]
 pub(crate) mod shape_set_queue_attributes;

+#[cfg(feature = "op_start_message_move_task")]
 pub(crate) mod shape_start_message_move_task;

+#[cfg(feature = "op_tag_queue")]
 pub(crate) mod shape_tag_queue;

+#[cfg(feature = "op_untag_queue")]
 pub(crate) mod shape_untag_queue;

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -91,150 +190,415 @@
     }
 }

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_batch_entry_ids_not_distinct;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_batch_request_too_long;

+#[cfg(feature = "op_cancel_message_move_task")]
 pub(crate) mod shape_cancel_message_move_task_input;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_input;

+#[cfg(feature = "op_change_message_visibility")]
 pub(crate) mod shape_change_message_visibility_input;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_create_queue_input;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_input;

+#[cfg(feature = "op_delete_message")]
 pub(crate) mod shape_delete_message_input;

+#[cfg(feature = "op_delete_queue")]
 pub(crate) mod shape_delete_queue_input;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_empty_batch_request;

+#[cfg(feature = "op_get_queue_attributes")]
 pub(crate) mod shape_get_queue_attributes_input;

+#[cfg(feature = "op_get_queue_url")]
 pub(crate) mod shape_get_queue_url_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_invalid_address;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 pub(crate) mod shape_invalid_attribute_name;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 pub(crate) mod shape_invalid_attribute_value;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_invalid_batch_entry_id;

+#[cfg(feature = "op_delete_message")]
 pub(crate) mod shape_invalid_id_format;

+#[cfg(feature = "op_send_message")]
 pub(crate) mod shape_invalid_message_contents;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_invalid_security;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_access_denied;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_disabled;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_invalid_key_usage;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_invalid_state;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_not_found;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_opt_in_required;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_kms_throttled;

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) mod shape_list_dead_letter_source_queues_input;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks_input;

+#[cfg(feature = "op_list_queue_tags")]
 pub(crate) mod shape_list_queue_tags_input;

+#[cfg(feature = "op_list_queues")]
 pub(crate) mod shape_list_queues_input;

+#[cfg(feature = "op_change_message_visibility")]
 pub(crate) mod shape_message_not_inflight;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub(crate) mod shape_over_limit;

+#[cfg(feature = "op_purge_queue")]
 pub(crate) mod shape_purge_queue_in_progress;

+#[cfg(feature = "op_purge_queue")]
 pub(crate) mod shape_purge_queue_input;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_queue_deleted_recently;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_queue_does_not_exist;

+#[cfg(feature = "op_create_queue")]
 pub(crate) mod shape_queue_name_exists;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 pub(crate) mod shape_receipt_handle_is_invalid;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_receive_message_input;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_request_throttled;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_input;

+#[cfg(feature = "op_send_message")]
 pub(crate) mod shape_send_message_input;

+#[cfg(feature = "op_set_queue_attributes")]
 pub(crate) mod shape_set_queue_attributes_input;

+#[cfg(feature = "op_start_message_move_task")]
 pub(crate) mod shape_start_message_move_task_input;

+#[cfg(feature = "op_tag_queue")]
 pub(crate) mod shape_tag_queue_input;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_too_many_entries_in_batch_request;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub(crate) mod shape_unsupported_operation;

+#[cfg(feature = "op_untag_queue")]
 pub(crate) mod shape_untag_queue_input;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_batch_result_error_entry_list;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_request_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_result_entry_list;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_request_entry;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_result_entry_list;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks_result_entry_list;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_message_attribute_value;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message_list;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub(crate) mod shape_message_system_attribute_value;

+#[cfg(feature = "op_get_queue_attributes")]
 pub(crate) mod shape_queue_attribute_map;

+#[cfg(any(feature = "op_list_dead_letter_source_queues", feature = "op_list_queues"))]
 pub(crate) mod shape_queue_url_list;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_request_entry;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_result_entry_list;

+#[cfg(feature = "op_list_queue_tags")]
 pub(crate) mod shape_tag_map;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_batch_result_error_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) mod shape_change_message_visibility_batch_result_entry;

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) mod shape_delete_message_batch_result_entry;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub(crate) mod shape_list_message_move_tasks_result_entry;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message;

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) mod shape_send_message_batch_result_entry;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message_body_attribute_map;

+#[cfg(feature = "op_receive_message")]
 pub(crate) mod shape_message_system_attribute_map;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_binary_list;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) mod shape_string_list;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) fn change_message_visibility_batch_output_output_correct_errors(
     mut builder: crate::operation::change_message_visibility_batch::builders::ChangeMessageVisibilityBatchOutputBuilder,
 ) -> crate::operation::change_message_visibility_batch::builders::ChangeMessageVisibilityBatchOutputBuilder {
@@ -11,6 +12,7 @@
     builder
 }

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) fn delete_message_batch_output_output_correct_errors(
     mut builder: crate::operation::delete_message_batch::builders::DeleteMessageBatchOutputBuilder,
 ) -> crate::operation::delete_message_batch::builders::DeleteMessageBatchOutputBuilder {
@@ -23,6 +25,7 @@
     builder
 }

+#[cfg(feature = "op_list_dead_letter_source_queues")]
 pub(crate) fn list_dead_letter_source_queues_output_output_correct_errors(
     mut builder: crate::operation::list_dead_letter_source_queues::builders::ListDeadLetterSourceQueuesOutputBuilder,
 ) -> crate::operation::list_dead_letter_source_queues::builders::ListDeadLetterSourceQueuesOutputBuilder {
@@ -32,6 +35,7 @@
     builder
 }

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) fn send_message_batch_output_output_correct_errors(
     mut builder: crate::operation::send_message_batch::builders::SendMessageBatchOutputBuilder,
 ) -> crate::operation::send_message_batch::builders::SendMessageBatchOutputBuilder {
@@ -44,6 +48,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub(crate) fn batch_result_error_entry_correct_errors(
     mut builder: crate::types::builders::BatchResultErrorEntryBuilder,
 ) -> crate::types::builders::BatchResultErrorEntryBuilder {
@@ -59,6 +68,7 @@
     builder
 }

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub(crate) fn change_message_visibility_batch_result_entry_correct_errors(
     mut builder: crate::types::builders::ChangeMessageVisibilityBatchResultEntryBuilder,
 ) -> crate::types::builders::ChangeMessageVisibilityBatchResultEntryBuilder {
@@ -68,6 +78,7 @@
     builder
 }

+#[cfg(feature = "op_delete_message_batch")]
 pub(crate) fn delete_message_batch_result_entry_correct_errors(
     mut builder: crate::types::builders::DeleteMessageBatchResultEntryBuilder,
 ) -> crate::types::builders::DeleteMessageBatchResultEntryBuilder {
@@ -77,6 +88,7 @@
     builder
 }

+#[cfg(feature = "op_send_message_batch")]
 pub(crate) fn send_message_batch_result_entry_correct_errors(
     mut builder: crate::types::builders::SendMessageBatchResultEntryBuilder,
 ) -> crate::types::builders::SendMessageBatchResultEntryBuilder {
@@ -92,6 +104,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub(crate) fn message_attribute_value_correct_errors(
     mut builder: crate::types::builders::MessageAttributeValueBuilder,
 ) -> crate::types::builders::MessageAttributeValueBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,58 +1,112 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_request_entry::ChangeMessageVisibilityBatchRequestEntry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_result_entry::ChangeMessageVisibilityBatchResultEntry;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntry;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::_queue_attribute_name::QueueAttributeName;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_request_entry::DeleteMessageBatchRequestEntry;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_result_entry::DeleteMessageBatchResultEntry;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub use crate::types::_list_message_move_tasks_result_entry::ListMessageMoveTasksResultEntry;

+#[cfg(feature = "op_receive_message")]
 pub use crate::types::_message_system_attribute_name::MessageSystemAttributeName;

+#[cfg(feature = "op_receive_message")]
 pub use crate::types::_message::Message;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_message_attribute_value::MessageAttributeValue;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub use crate::types::_message_system_attribute_name_for_sends::MessageSystemAttributeNameForSends;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub use crate::types::_message_system_attribute_value::MessageSystemAttributeValue;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_request_entry::SendMessageBatchRequestEntry;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_result_entry::SendMessageBatchResultEntry;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _batch_result_error_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 mod _change_message_visibility_batch_request_entry;

+#[cfg(feature = "op_change_message_visibility_batch")]
 mod _change_message_visibility_batch_result_entry;

+#[cfg(feature = "op_delete_message_batch")]
 mod _delete_message_batch_request_entry;

+#[cfg(feature = "op_delete_message_batch")]
 mod _delete_message_batch_result_entry;

+#[cfg(feature = "op_list_message_move_tasks")]
 mod _list_message_move_tasks_result_entry;

+#[cfg(feature = "op_receive_message")]
 mod _message;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _message_attribute_value;

+#[cfg(feature = "op_receive_message")]
 mod _message_system_attribute_name;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 mod _message_system_attribute_name_for_sends;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 mod _message_system_attribute_value;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 mod _queue_attribute_name;

+#[cfg(feature = "op_send_message_batch")]
 mod _send_message_batch_request_entry;

+#[cfg(feature = "op_send_message_batch")]
 mod _send_message_batch_result_entry;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,22 +1,41 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_request_entry::ChangeMessageVisibilityBatchRequestEntryBuilder;

+#[cfg(feature = "op_change_message_visibility_batch")]
 pub use crate::types::_change_message_visibility_batch_result_entry::ChangeMessageVisibilityBatchResultEntryBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntryBuilder;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_request_entry::DeleteMessageBatchRequestEntryBuilder;

+#[cfg(feature = "op_delete_message_batch")]
 pub use crate::types::_delete_message_batch_result_entry::DeleteMessageBatchResultEntryBuilder;

+#[cfg(feature = "op_list_message_move_tasks")]
 pub use crate::types::_list_message_move_tasks_result_entry::ListMessageMoveTasksResultEntryBuilder;

+#[cfg(feature = "op_receive_message")]
 pub use crate::types::_message::MessageBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::_message_attribute_value::MessageAttributeValueBuilder;

+#[cfg(any(feature = "op_send_message", feature = "op_send_message_batch"))]
 pub use crate::types::_message_system_attribute_value::MessageSystemAttributeValueBuilder;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_request_entry::SendMessageBatchRequestEntryBuilder;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::_send_message_batch_result_entry::SendMessageBatchResultEntryBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,114 +1,512 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_address::InvalidAddress;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_security::InvalidSecurity;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_over_limit::OverLimit;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_queue_does_not_exist::QueueDoesNotExist;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_request_throttled::RequestThrottled;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_unsupported_operation::UnsupportedOperation;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(feature = "op_change_message_visibility")]
 pub use crate::types::error::_message_not_inflight::MessageNotInflight;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 pub use crate::types::error::_receipt_handle_is_invalid::ReceiptHandleIsInvalid;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_batch_entry_ids_not_distinct::BatchEntryIdsNotDistinct;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_empty_batch_request::EmptyBatchRequest;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_invalid_batch_entry_id::InvalidBatchEntryId;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_too_many_entries_in_batch_request::TooManyEntriesInBatchRequest;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_invalid_attribute_name::InvalidAttributeName;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 pub use crate::types::error::_invalid_attribute_value::InvalidAttributeValue;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_deleted_recently::QueueDeletedRecently;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_name_exists::QueueNameExists;

+#[cfg(feature = "op_delete_message")]
 pub use crate::types::error::_invalid_id_format::InvalidIdFormat;

+#[cfg(feature = "op_purge_queue")]
 pub use crate::types::error::_purge_queue_in_progress::PurgeQueueInProgress;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_access_denied::KmsAccessDenied;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_disabled::KmsDisabled;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_key_usage::KmsInvalidKeyUsage;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_state::KmsInvalidState;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_not_found::KmsNotFound;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequired;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_throttled::KmsThrottled;

+#[cfg(feature = "op_send_message")]
 pub use crate::types::error::_invalid_message_contents::InvalidMessageContents;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::error::_batch_request_too_long::BatchRequestTooLong;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _batch_entry_ids_not_distinct;

+#[cfg(feature = "op_send_message_batch")]
 mod _batch_request_too_long;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _empty_batch_request;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _invalid_address;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 mod _invalid_attribute_name;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 mod _invalid_attribute_value;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _invalid_batch_entry_id;

+#[cfg(feature = "op_delete_message")]
 mod _invalid_id_format;

+#[cfg(feature = "op_send_message")]
 mod _invalid_message_contents;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _invalid_security;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_access_denied;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_disabled;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_invalid_key_usage;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_invalid_state;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_not_found;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_opt_in_required;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 mod _kms_throttled;

+#[cfg(feature = "op_change_message_visibility")]
 mod _message_not_inflight;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 mod _over_limit;

+#[cfg(feature = "op_purge_queue")]
 mod _purge_queue_in_progress;

+#[cfg(feature = "op_create_queue")]
 mod _queue_deleted_recently;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _queue_does_not_exist;

+#[cfg(feature = "op_create_queue")]
 mod _queue_name_exists;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 mod _receipt_handle_is_invalid;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _request_throttled;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 mod _too_many_entries_in_batch_request;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 mod _unsupported_operation;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,56 +1,255 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_address::InvalidAddressBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_invalid_security::InvalidSecurityBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_receive_message",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_over_limit::OverLimitBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_queue_tags",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_queue_does_not_exist::QueueDoesNotExistBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_request_throttled::RequestThrottledBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_cancel_message_move_task",
+    feature = "op_change_message_visibility",
+    feature = "op_change_message_visibility_batch",
+    feature = "op_create_queue",
+    feature = "op_delete_message",
+    feature = "op_delete_message_batch",
+    feature = "op_delete_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_get_queue_url",
+    feature = "op_list_dead_letter_source_queues",
+    feature = "op_list_message_move_tasks",
+    feature = "op_list_queue_tags",
+    feature = "op_list_queues",
+    feature = "op_purge_queue",
+    feature = "op_receive_message",
+    feature = "op_remove_permission",
+    feature = "op_send_message",
+    feature = "op_send_message_batch",
+    feature = "op_set_queue_attributes",
+    feature = "op_start_message_move_task",
+    feature = "op_tag_queue",
+    feature = "op_untag_queue"
+))]
 pub use crate::types::error::_unsupported_operation::UnsupportedOperationBuilder;

+#[cfg(any(
+    feature = "op_cancel_message_move_task",
+    feature = "op_list_message_move_tasks",
+    feature = "op_start_message_move_task"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(feature = "op_change_message_visibility")]
 pub use crate::types::error::_message_not_inflight::MessageNotInflightBuilder;

+#[cfg(any(feature = "op_change_message_visibility", feature = "op_delete_message"))]
 pub use crate::types::error::_receipt_handle_is_invalid::ReceiptHandleIsInvalidBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_batch_entry_ids_not_distinct::BatchEntryIdsNotDistinctBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_empty_batch_request::EmptyBatchRequestBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_invalid_batch_entry_id::InvalidBatchEntryIdBuilder;

+#[cfg(any(
+    feature = "op_change_message_visibility_batch",
+    feature = "op_delete_message_batch",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_too_many_entries_in_batch_request::TooManyEntriesInBatchRequestBuilder;

+#[cfg(any(
+    feature = "op_create_queue",
+    feature = "op_get_queue_attributes",
+    feature = "op_set_queue_attributes"
+))]
 pub use crate::types::error::_invalid_attribute_name::InvalidAttributeNameBuilder;

+#[cfg(any(feature = "op_create_queue", feature = "op_set_queue_attributes"))]
 pub use crate::types::error::_invalid_attribute_value::InvalidAttributeValueBuilder;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_deleted_recently::QueueDeletedRecentlyBuilder;

+#[cfg(feature = "op_create_queue")]
 pub use crate::types::error::_queue_name_exists::QueueNameExistsBuilder;

+#[cfg(feature = "op_delete_message")]
 pub use crate::types::error::_invalid_id_format::InvalidIdFormatBuilder;

+#[cfg(feature = "op_purge_queue")]
 pub use crate::types::error::_purge_queue_in_progress::PurgeQueueInProgressBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_access_denied::KmsAccessDeniedBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_disabled::KmsDisabledBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_key_usage::KmsInvalidKeyUsageBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_invalid_state::KmsInvalidStateBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_not_found::KmsNotFoundBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequiredBuilder;

+#[cfg(any(
+    feature = "op_receive_message",
+    feature = "op_send_message",
+    feature = "op_send_message_batch"
+))]
 pub use crate::types::error::_kms_throttled::KmsThrottledBuilder;

+#[cfg(feature = "op_send_message")]
 pub use crate::types::error::_invalid_message_contents::InvalidMessageContentsBuilder;

+#[cfg(feature = "op_send_message_batch")]
 pub use crate::types::error::_batch_request_too_long::BatchRequestTooLongBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
