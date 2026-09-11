# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/sso`
- model: `aws-models/sso.json`
- package: `aws-sdk-sso`
- library: `aws_sdk_sso`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_get_role_credentials`: `GetRoleCredentials`
- `op_list_account_roles`: `ListAccountRoles`
- `op_list_accounts`: `ListAccounts`
- `op_logout`: `Logout`

## Changed files

- `Cargo.toml`
- `src/client.rs`
- `src/error_meta.rs`
- `src/lens.rs`
- `src/operation.rs`
- `src/protocol_serde.rs`
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
@@ -84,7 +73,6 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

@@ -103,3 +91,7 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_get_role_credentials = []
+op_list_account_roles = []
+op_list_accounts = []
+op_logout = []
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -117,10 +117,14 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_get_role_credentials")]
 mod get_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 mod list_account_roles;

+#[cfg(feature = "op_list_accounts")]
 mod list_accounts;

+#[cfg(feature = "op_logout")]
 mod logout;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,12 +3,35 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts",
+        feature = "op_logout"
+    ))]
     /// <p>Indicates that a problem occurred with the input to the request. For example, a required parameter might be missing or out of range.</p>
     InvalidRequestException(crate::types::error::InvalidRequestException),
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts"
+    ))]
     /// <p>The specified resource doesn't exist.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts",
+        feature = "op_logout"
+    ))]
     /// <p>Indicates that the request is being made too frequently and is more than what the server can handle.</p>
     TooManyRequestsException(crate::types::error::TooManyRequestsException),
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts",
+        feature = "op_logout"
+    ))]
     /// <p>Indicates that the request is not authorized. This can happen due to an invalid access token in the request.</p>
     UnauthorizedException(crate::types::error::UnauthorizedException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -25,9 +48,32 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::InvalidRequestException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::TooManyRequestsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::UnauthorizedException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -52,14 +98,38 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::InvalidRequestException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::TooManyRequestsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::UnauthorizedException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_get_role_credentials")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -85,6 +155,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_role_credentials")]
 impl From<crate::operation::get_role_credentials::GetRoleCredentialsError> for Error {
     fn from(err: crate::operation::get_role_credentials::GetRoleCredentialsError) -> Self {
         match err {
@@ -106,6 +177,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_account_roles")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -131,6 +203,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_account_roles")]
 impl From<crate::operation::list_account_roles::ListAccountRolesError> for Error {
     fn from(err: crate::operation::list_account_roles::ListAccountRolesError) -> Self {
         match err {
@@ -150,6 +223,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_accounts")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_accounts::ListAccountsError, R>>
     for Error
 where
@@ -167,6 +241,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_accounts")]
 impl From<crate::operation::list_accounts::ListAccountsError> for Error {
     fn from(err: crate::operation::list_accounts::ListAccountsError) -> Self {
         match err {
@@ -186,6 +261,7 @@
         }
     }
 }
+#[cfg(feature = "op_logout")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::logout::LogoutError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -200,6 +276,7 @@
         }
     }
 }
+#[cfg(feature = "op_logout")]
 impl From<crate::operation::logout::LogoutError> for Error {
     fn from(err: crate::operation::logout::LogoutError) -> Self {
         match err {
@@ -217,9 +294,32 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::InvalidRequestException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::TooManyRequestsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::UnauthorizedException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -228,9 +328,32 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::InvalidRequestException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::TooManyRequestsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::UnauthorizedException(e) => e.request_id(),
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
+#[cfg(feature = "op_list_account_roles")]
 pub(crate) fn reflens_list_account_roles_output_output_next_token(
     input: &crate::operation::list_account_roles::ListAccountRolesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_accounts")]
 pub(crate) fn reflens_list_accounts_output_output_next_token(
     input: &crate::operation::list_accounts::ListAccountsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) fn lens_list_account_roles_output_output_role_list(
     input: crate::operation::list_account_roles::ListAccountRolesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::RoleInfo>> {
@@ -26,6 +29,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_accounts")]
 pub(crate) fn lens_list_accounts_output_output_account_list(
     input: crate::operation::list_accounts::ListAccountsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AccountInfo>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,14 +1,18 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_get_role_credentials")]
 /// Types for the `GetRoleCredentials` operation.
 pub mod get_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 /// Types for the `ListAccountRoles` operation.
 pub mod list_account_roles;

+#[cfg(feature = "op_list_accounts")]
 /// Types for the `ListAccounts` operation.
 pub mod list_accounts;

+#[cfg(feature = "op_logout")]
 /// Types for the `Logout` operation.
 pub mod logout;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,10 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +23,12 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,14 +40,24 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_get_role_credentials")]
 pub(crate) mod shape_get_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) mod shape_list_account_roles;

+#[cfg(feature = "op_list_accounts")]
 pub(crate) mod shape_list_accounts;

+#[cfg(feature = "op_logout")]
 pub(crate) mod shape_logout;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -44,20 +66,48 @@
     }
 }

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) mod shape_invalid_request_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) mod shape_too_many_requests_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) mod shape_unauthorized_exception;

+#[cfg(feature = "op_list_accounts")]
 pub(crate) mod shape_account_list_type;

+#[cfg(feature = "op_get_role_credentials")]
 pub(crate) mod shape_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) mod shape_role_list_type;

+#[cfg(feature = "op_list_accounts")]
 pub(crate) mod shape_account_info;

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) mod shape_role_info;
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,14 +1,20 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_role_credentials")]
 pub use crate::types::_role_credentials::RoleCredentials;

+#[cfg(feature = "op_list_account_roles")]
 pub use crate::types::_role_info::RoleInfo;

+#[cfg(feature = "op_list_accounts")]
 pub use crate::types::_account_info::AccountInfo;

+#[cfg(feature = "op_list_accounts")]
 mod _account_info;

+#[cfg(feature = "op_get_role_credentials")]
 mod _role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 mod _role_info;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,6 +1,9 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_role_credentials")]
 pub use crate::types::_role_credentials::RoleCredentialsBuilder;

+#[cfg(feature = "op_list_account_roles")]
 pub use crate::types::_role_info::RoleInfoBuilder;

+#[cfg(feature = "op_list_accounts")]
 pub use crate::types::_account_info::AccountInfoBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,18 +1,64 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_invalid_request_exception::InvalidRequestException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_unauthorized_exception::UnauthorizedException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 mod _invalid_request_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 mod _too_many_requests_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 mod _unauthorized_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,8 +1,31 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_invalid_request_exception::InvalidRequestExceptionBuilder;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsExceptionBuilder;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_unauthorized_exception::UnauthorizedExceptionBuilder;
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
@@ -84,7 +73,6 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

@@ -103,3 +91,7 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_get_role_credentials = []
+op_list_account_roles = []
+op_list_accounts = []
+op_logout = []
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -117,10 +117,14 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_get_role_credentials")]
 mod get_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 mod list_account_roles;

+#[cfg(feature = "op_list_accounts")]
 mod list_accounts;

+#[cfg(feature = "op_logout")]
 mod logout;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,12 +3,35 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts",
+        feature = "op_logout"
+    ))]
     /// <p>Indicates that a problem occurred with the input to the request. For example, a required parameter might be missing or out of range.</p>
     InvalidRequestException(crate::types::error::InvalidRequestException),
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts"
+    ))]
     /// <p>The specified resource doesn't exist.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts",
+        feature = "op_logout"
+    ))]
     /// <p>Indicates that the request is being made too frequently and is more than what the server can handle.</p>
     TooManyRequestsException(crate::types::error::TooManyRequestsException),
+    #[cfg(any(
+        feature = "op_get_role_credentials",
+        feature = "op_list_account_roles",
+        feature = "op_list_accounts",
+        feature = "op_logout"
+    ))]
     /// <p>Indicates that the request is not authorized. This can happen due to an invalid access token in the request.</p>
     UnauthorizedException(crate::types::error::UnauthorizedException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -25,9 +48,32 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::InvalidRequestException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::TooManyRequestsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::UnauthorizedException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -52,14 +98,38 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::InvalidRequestException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::TooManyRequestsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::UnauthorizedException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_get_role_credentials")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -85,6 +155,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_role_credentials")]
 impl From<crate::operation::get_role_credentials::GetRoleCredentialsError> for Error {
     fn from(err: crate::operation::get_role_credentials::GetRoleCredentialsError) -> Self {
         match err {
@@ -106,6 +177,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_account_roles")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -131,6 +203,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_account_roles")]
 impl From<crate::operation::list_account_roles::ListAccountRolesError> for Error {
     fn from(err: crate::operation::list_account_roles::ListAccountRolesError) -> Self {
         match err {
@@ -150,6 +223,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_accounts")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_accounts::ListAccountsError, R>>
     for Error
 where
@@ -167,6 +241,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_accounts")]
 impl From<crate::operation::list_accounts::ListAccountsError> for Error {
     fn from(err: crate::operation::list_accounts::ListAccountsError) -> Self {
         match err {
@@ -186,6 +261,7 @@
         }
     }
 }
+#[cfg(feature = "op_logout")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::logout::LogoutError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -200,6 +276,7 @@
         }
     }
 }
+#[cfg(feature = "op_logout")]
 impl From<crate::operation::logout::LogoutError> for Error {
     fn from(err: crate::operation::logout::LogoutError) -> Self {
         match err {
@@ -217,9 +294,32 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::InvalidRequestException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::TooManyRequestsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Error::UnauthorizedException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -228,9 +328,32 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::InvalidRequestException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::TooManyRequestsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_get_role_credentials",
+                feature = "op_list_account_roles",
+                feature = "op_list_accounts",
+                feature = "op_logout"
+            ))]
             Self::UnauthorizedException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_list_account_roles")]
 pub(crate) fn reflens_list_account_roles_output_output_next_token(
     input: &crate::operation::list_account_roles::ListAccountRolesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_accounts")]
 pub(crate) fn reflens_list_accounts_output_output_next_token(
     input: &crate::operation::list_accounts::ListAccountsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) fn lens_list_account_roles_output_output_role_list(
     input: crate::operation::list_account_roles::ListAccountRolesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::RoleInfo>> {
@@ -26,6 +29,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_accounts")]
 pub(crate) fn lens_list_accounts_output_output_account_list(
     input: crate::operation::list_accounts::ListAccountsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AccountInfo>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,14 +1,18 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_get_role_credentials")]
 /// Types for the `GetRoleCredentials` operation.
 pub mod get_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 /// Types for the `ListAccountRoles` operation.
 pub mod list_account_roles;

+#[cfg(feature = "op_list_accounts")]
 /// Types for the `ListAccounts` operation.
 pub mod list_accounts;

+#[cfg(feature = "op_logout")]
 /// Types for the `Logout` operation.
 pub mod logout;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,10 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +23,12 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,14 +40,24 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_get_role_credentials")]
 pub(crate) mod shape_get_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) mod shape_list_account_roles;

+#[cfg(feature = "op_list_accounts")]
 pub(crate) mod shape_list_accounts;

+#[cfg(feature = "op_logout")]
 pub(crate) mod shape_logout;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -44,20 +66,48 @@
     }
 }

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) mod shape_invalid_request_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) mod shape_too_many_requests_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub(crate) mod shape_unauthorized_exception;

+#[cfg(feature = "op_list_accounts")]
 pub(crate) mod shape_account_list_type;

+#[cfg(feature = "op_get_role_credentials")]
 pub(crate) mod shape_role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) mod shape_role_list_type;

+#[cfg(feature = "op_list_accounts")]
 pub(crate) mod shape_account_info;

+#[cfg(feature = "op_list_account_roles")]
 pub(crate) mod shape_role_info;
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,14 +1,20 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_role_credentials")]
 pub use crate::types::_role_credentials::RoleCredentials;

+#[cfg(feature = "op_list_account_roles")]
 pub use crate::types::_role_info::RoleInfo;

+#[cfg(feature = "op_list_accounts")]
 pub use crate::types::_account_info::AccountInfo;

+#[cfg(feature = "op_list_accounts")]
 mod _account_info;

+#[cfg(feature = "op_get_role_credentials")]
 mod _role_credentials;

+#[cfg(feature = "op_list_account_roles")]
 mod _role_info;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,6 +1,9 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_role_credentials")]
 pub use crate::types::_role_credentials::RoleCredentialsBuilder;

+#[cfg(feature = "op_list_account_roles")]
 pub use crate::types::_role_info::RoleInfoBuilder;

+#[cfg(feature = "op_list_accounts")]
 pub use crate::types::_account_info::AccountInfoBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,18 +1,64 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_invalid_request_exception::InvalidRequestException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_unauthorized_exception::UnauthorizedException;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 mod _invalid_request_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 mod _too_many_requests_exception;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 mod _unauthorized_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,8 +1,31 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_invalid_request_exception::InvalidRequestExceptionBuilder;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsExceptionBuilder;

+#[cfg(any(
+    feature = "op_get_role_credentials",
+    feature = "op_list_account_roles",
+    feature = "op_list_accounts",
+    feature = "op_logout"
+))]
 pub use crate::types::error::_unauthorized_exception::UnauthorizedExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
