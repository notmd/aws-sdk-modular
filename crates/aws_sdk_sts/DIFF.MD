# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/sts`
- model: `aws-models/sts.json`
- package: `aws-sdk-sts`
- library: `aws_sdk_sts`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_assume_role`: `AssumeRole`
- `op_assume_role_with_saml`: `AssumeRoleWithSAML`
- `op_assume_role_with_web_identity`: `AssumeRoleWithWebIdentity`
- `op_assume_root`: `AssumeRoot`
- `op_decode_authorization_message`: `DecodeAuthorizationMessage`
- `op_get_access_key_info`: `GetAccessKeyInfo`
- `op_get_caller_identity`: `GetCallerIdentity`
- `op_get_delegated_access_token`: `GetDelegatedAccessToken`
- `op_get_federation_token`: `GetFederationToken`
- `op_get_session_token`: `GetSessionToken`
- `op_get_web_identity_token`: `GetWebIdentityToken`

## Changed files

- `Cargo.toml`
- `src/client.rs`
- `src/error_meta.rs`
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
@@ -89,41 +76,33 @@
 [dependencies.tracing]
 version = "0.1"
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

@@ -155,6 +134,17 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["sigv4a", "rustls", "default-https-client", "rt-tokio"]
+op_assume_role = []
+op_assume_role_with_saml = []
+op_assume_role_with_web_identity = []
+op_assume_root = []
+op_decode_authorization_message = []
+op_get_access_key_info = []
+op_get_caller_identity = []
+op_get_delegated_access_token = []
+op_get_federation_token = []
+op_get_session_token = []
+op_get_web_identity_token = []

 [hints]
 mostly-unused = true
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -90,12 +90,16 @@
     }
 }

+#[cfg(feature = "op_assume_role")]
 mod assume_role;

+#[cfg(feature = "op_assume_role_with_saml")]
 mod assume_role_with_saml;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 mod assume_role_with_web_identity;

+#[cfg(feature = "op_assume_root")]
 mod assume_root;

 /// Operation customization and supporting types.
@@ -125,16 +129,23 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_decode_authorization_message")]
 mod decode_authorization_message;

+#[cfg(feature = "op_get_access_key_info")]
 mod get_access_key_info;

+#[cfg(feature = "op_get_caller_identity")]
 mod get_caller_identity;

+#[cfg(feature = "op_get_delegated_access_token")]
 mod get_delegated_access_token;

+#[cfg(feature = "op_get_federation_token")]
 mod get_federation_token;

+#[cfg(feature = "op_get_session_token")]
 mod get_session_token;

+#[cfg(feature = "op_get_web_identity_token")]
 mod get_web_identity_token;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,30 +3,66 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_assume_root"
+    ))]
     /// <p>The web identity token that was passed is expired or is not valid. Get a new identity token from the identity provider and then retry the request.</p>
     ExpiredTokenException(crate::types::error::ExpiredTokenException),
+    #[cfg(feature = "op_get_delegated_access_token")]
     /// <p>The trade-in token provided in the request has expired and can no longer be exchanged for credentials. Request a new token and retry the operation.</p>
     ExpiredTradeInTokenException(crate::types::error::ExpiredTradeInTokenException),
+    #[cfg(feature = "op_assume_role_with_web_identity")]
     /// <p>The request could not be fulfilled because the identity provider (IDP) that was asked to verify the incoming identity token could not be reached. This is often a transient error caused by network conditions. Retry the request a limited number of times so that you don't exceed the request rate. If the error persists, the identity provider might be down or not responding.</p>
     IdpCommunicationErrorException(crate::types::error::IdpCommunicationErrorException),
+    #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
     /// <p>The identity provider (IdP) reported that authentication failed. This might be because the claim is invalid.</p>
     /// <p>If this error is returned for the <code>AssumeRoleWithWebIdentity</code> operation, it can also mean that the claim has expired or has been explicitly revoked.</p>
     IdpRejectedClaimException(crate::types::error::IdpRejectedClaimException),
+    #[cfg(feature = "op_decode_authorization_message")]
     /// <p>The error returned if the message passed to <code>DecodeAuthorizationMessage</code> was invalid. This can happen if the token contains invalid characters, such as line breaks, or if the message has expired.</p>
     InvalidAuthorizationMessageException(crate::types::error::InvalidAuthorizationMessageException),
+    #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
     /// <p>The web identity token that was passed could not be validated by Amazon Web Services. Get a new identity token from the identity provider and then retry the request.</p>
     InvalidIdentityTokenException(crate::types::error::InvalidIdentityTokenException),
+    #[cfg(feature = "op_get_web_identity_token")]
     /// <p>The requested token payload size exceeds the maximum allowed size. Reduce the number of request tags included in the <code>GetWebIdentityToken</code> API call to reduce the token payload size.</p>
     JwtPayloadSizeExceededException(crate::types::error::JwtPayloadSizeExceededException),
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_get_federation_token"
+    ))]
     /// <p>The request was rejected because the policy document was malformed. The error message describes the specific error.</p>
     MalformedPolicyDocumentException(crate::types::error::MalformedPolicyDocumentException),
+    #[cfg(feature = "op_get_web_identity_token")]
     /// <p>The outbound web identity federation feature is not enabled for this account. To use this feature, you must first enable it through the Amazon Web Services Management Console or API.</p>
     OutboundWebIdentityFederationDisabledException(crate::types::error::OutboundWebIdentityFederationDisabledException),
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_get_delegated_access_token",
+        feature = "op_get_federation_token"
+    ))]
     /// <p>The request was rejected because the total packed size of the session policies and session tags combined was too large. An Amazon Web Services conversion compresses the session policy document, session policy ARNs, and session tags into a packed binary format that has a separate limit. The error message indicates by percentage how close the policies and tags are to the upper size limit. For more information, see <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_session-tags.html">Passing Session Tags in STS</a> in the <i>IAM User Guide</i>.</p>
     /// <p>You could receive this error even though you meet other defined session policy and session tag limits. For more information, see <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html#reference_iam-limits-entity-length">IAM and STS Entity Character Limits</a> in the <i>IAM User Guide</i>.</p>
     PackedPolicyTooLargeException(crate::types::error::PackedPolicyTooLargeException),
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_assume_root",
+        feature = "op_get_delegated_access_token",
+        feature = "op_get_federation_token",
+        feature = "op_get_session_token"
+    ))]
     /// <p>STS is not activated in the requested region for the account that is being asked to generate credentials. The account administrator must use the IAM console to activate STS in that region. For more information, see <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp_enable-regions.html#sts-regions-activate-deactivate">Activating and Deactivating STS in an Amazon Web Services Region</a> in the <i>IAM User Guide</i>.</p>
     RegionDisabledException(crate::types::error::RegionDisabledException),
+    #[cfg(feature = "op_get_web_identity_token")]
     /// <p>The requested token duration would extend the session beyond its original expiration time. You cannot use this operation to extend the lifetime of a session beyond what was granted when the session was originally created.</p>
     SessionDurationEscalationException(crate::types::error::SessionDurationEscalationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -43,17 +79,53 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Error::ExpiredTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Error::ExpiredTradeInTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Error::IdpCommunicationErrorException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::IdpRejectedClaimException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_decode_authorization_message")]
             Error::InvalidAuthorizationMessageException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::InvalidIdentityTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::JwtPayloadSizeExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::OutboundWebIdentityFederationDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Error::PackedPolicyTooLargeException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Error::RegionDisabledException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::SessionDurationEscalationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -78,22 +150,59 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Self::ExpiredTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Self::ExpiredTradeInTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Self::IdpCommunicationErrorException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::IdpRejectedClaimException(inner) => inner.meta(),
+            #[cfg(feature = "op_decode_authorization_message")]
             Self::InvalidAuthorizationMessageException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::InvalidIdentityTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::JwtPayloadSizeExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Self::MalformedPolicyDocumentException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::OutboundWebIdentityFederationDisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Self::PackedPolicyTooLargeException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Self::RegionDisabledException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::SessionDurationEscalationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_assume_role")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::assume_role::AssumeRoleError, R>>
     for Error
 where
@@ -111,6 +220,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role")]
 impl From<crate::operation::assume_role::AssumeRoleError> for Error {
     fn from(err: crate::operation::assume_role::AssumeRoleError) -> Self {
         match err {
@@ -130,6 +240,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_saml")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -155,6 +266,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_saml")]
 impl From<crate::operation::assume_role_with_saml::AssumeRoleWithSAMLError> for Error {
     fn from(err: crate::operation::assume_role_with_saml::AssumeRoleWithSAMLError) -> Self {
         match err {
@@ -182,6 +294,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_web_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -207,6 +320,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_web_identity")]
 impl From<crate::operation::assume_role_with_web_identity::AssumeRoleWithWebIdentityError> for Error {
     fn from(err: crate::operation::assume_role_with_web_identity::AssumeRoleWithWebIdentityError) -> Self {
         match err {
@@ -235,6 +349,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_root")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::assume_root::AssumeRootError, R>>
     for Error
 where
@@ -252,6 +367,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_root")]
 impl From<crate::operation::assume_root::AssumeRootError> for Error {
     fn from(err: crate::operation::assume_root::AssumeRootError) -> Self {
         match err {
@@ -265,6 +381,7 @@
         }
     }
 }
+#[cfg(feature = "op_decode_authorization_message")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -290,6 +407,7 @@
         }
     }
 }
+#[cfg(feature = "op_decode_authorization_message")]
 impl From<crate::operation::decode_authorization_message::DecodeAuthorizationMessageError> for Error {
     fn from(err: crate::operation::decode_authorization_message::DecodeAuthorizationMessageError) -> Self {
         match err {
@@ -300,6 +418,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_access_key_info")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -325,6 +444,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_access_key_info")]
 impl From<crate::operation::get_access_key_info::GetAccessKeyInfoError> for Error {
     fn from(err: crate::operation::get_access_key_info::GetAccessKeyInfoError) -> Self {
         match err {
@@ -332,6 +452,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_caller_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -357,6 +478,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_caller_identity")]
 impl From<crate::operation::get_caller_identity::GetCallerIdentityError> for Error {
     fn from(err: crate::operation::get_caller_identity::GetCallerIdentityError) -> Self {
         match err {
@@ -364,6 +486,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delegated_access_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -389,6 +512,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delegated_access_token")]
 impl From<crate::operation::get_delegated_access_token::GetDelegatedAccessTokenError> for Error {
     fn from(err: crate::operation::get_delegated_access_token::GetDelegatedAccessTokenError) -> Self {
         match err {
@@ -405,6 +529,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_federation_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -430,6 +555,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_federation_token")]
 impl From<crate::operation::get_federation_token::GetFederationTokenError> for Error {
     fn from(err: crate::operation::get_federation_token::GetFederationTokenError) -> Self {
         match err {
@@ -448,6 +574,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_session_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -473,6 +600,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_session_token")]
 impl From<crate::operation::get_session_token::GetSessionTokenError> for Error {
     fn from(err: crate::operation::get_session_token::GetSessionTokenError) -> Self {
         match err {
@@ -483,6 +611,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_web_identity_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -508,6 +637,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_web_identity_token")]
 impl From<crate::operation::get_web_identity_token::GetWebIdentityTokenError> for Error {
     fn from(err: crate::operation::get_web_identity_token::GetWebIdentityTokenError) -> Self {
         match err {
@@ -527,17 +657,53 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Error::ExpiredTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Error::ExpiredTradeInTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Error::IdpCommunicationErrorException(inner) => inner.source(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::IdpRejectedClaimException(inner) => inner.source(),
+            #[cfg(feature = "op_decode_authorization_message")]
             Error::InvalidAuthorizationMessageException(inner) => inner.source(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::InvalidIdentityTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::JwtPayloadSizeExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.source(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::OutboundWebIdentityFederationDisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Error::PackedPolicyTooLargeException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Error::RegionDisabledException(inner) => inner.source(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::SessionDurationEscalationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -546,17 +712,53 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Self::ExpiredTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Self::ExpiredTradeInTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Self::IdpCommunicationErrorException(e) => e.request_id(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::IdpRejectedClaimException(e) => e.request_id(),
+            #[cfg(feature = "op_decode_authorization_message")]
             Self::InvalidAuthorizationMessageException(e) => e.request_id(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::InvalidIdentityTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::JwtPayloadSizeExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Self::MalformedPolicyDocumentException(e) => e.request_id(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::OutboundWebIdentityFederationDisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Self::PackedPolicyTooLargeException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Self::RegionDisabledException(e) => e.request_id(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::SessionDurationEscalationException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,35 +1,46 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_assume_role")]
 /// Types for the `AssumeRole` operation.
 pub mod assume_role;

+#[cfg(feature = "op_assume_role_with_saml")]
 /// Types for the `AssumeRoleWithSAML` operation.
 pub mod assume_role_with_saml;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 /// Types for the `AssumeRoleWithWebIdentity` operation.
 pub mod assume_role_with_web_identity;

+#[cfg(feature = "op_assume_root")]
 /// Types for the `AssumeRoot` operation.
 pub mod assume_root;

+#[cfg(feature = "op_decode_authorization_message")]
 /// Types for the `DecodeAuthorizationMessage` operation.
 pub mod decode_authorization_message;

+#[cfg(feature = "op_get_access_key_info")]
 /// Types for the `GetAccessKeyInfo` operation.
 pub mod get_access_key_info;

+#[cfg(feature = "op_get_caller_identity")]
 /// Types for the `GetCallerIdentity` operation.
 pub mod get_caller_identity;

+#[cfg(feature = "op_get_delegated_access_token")]
 /// Types for the `GetDelegatedAccessToken` operation.
 pub mod get_delegated_access_token;

+#[cfg(feature = "op_get_federation_token")]
 /// Types for the `GetFederationToken` operation.
 pub mod get_federation_token;

+#[cfg(feature = "op_get_session_token")]
 /// Types for the `GetSessionToken` operation.
 pub mod get_session_token;

+#[cfg(feature = "op_get_web_identity_token")]
 /// Types for the `GetWebIdentityToken` operation.
 pub mod get_web_identity_token;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,17 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_decode_authorization_message",
+    feature = "op_get_access_key_info",
+    feature = "op_get_caller_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token",
+    feature = "op_get_web_identity_token"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +30,19 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_decode_authorization_message",
+    feature = "op_get_access_key_info",
+    feature = "op_get_caller_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token",
+    feature = "op_get_web_identity_token"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     _response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -25,82 +51,168 @@
     crate::rest_xml_wrapped_errors::parse_error_metadata(response_body)
 }

+#[cfg(feature = "op_assume_role")]
 pub(crate) mod shape_assume_role;

+#[cfg(feature = "op_assume_role")]
 pub(crate) mod shape_assume_role_input;

+#[cfg(feature = "op_assume_role_with_saml")]
 pub(crate) mod shape_assume_role_with_saml;

+#[cfg(feature = "op_assume_role_with_saml")]
 pub(crate) mod shape_assume_role_with_saml_input;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub(crate) mod shape_assume_role_with_web_identity;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub(crate) mod shape_assume_role_with_web_identity_input;

+#[cfg(feature = "op_assume_root")]
 pub(crate) mod shape_assume_root;

+#[cfg(feature = "op_assume_root")]
 pub(crate) mod shape_assume_root_input;

+#[cfg(feature = "op_decode_authorization_message")]
 pub(crate) mod shape_decode_authorization_message;

+#[cfg(feature = "op_decode_authorization_message")]
 pub(crate) mod shape_decode_authorization_message_input;

+#[cfg(feature = "op_get_access_key_info")]
 pub(crate) mod shape_get_access_key_info;

+#[cfg(feature = "op_get_access_key_info")]
 pub(crate) mod shape_get_access_key_info_input;

+#[cfg(feature = "op_get_caller_identity")]
 pub(crate) mod shape_get_caller_identity;

+#[cfg(feature = "op_get_caller_identity")]
 pub(crate) mod shape_get_caller_identity_input;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub(crate) mod shape_get_delegated_access_token;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub(crate) mod shape_get_delegated_access_token_input;

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) mod shape_get_federation_token;

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) mod shape_get_federation_token_input;

+#[cfg(feature = "op_get_session_token")]
 pub(crate) mod shape_get_session_token;

+#[cfg(feature = "op_get_session_token")]
 pub(crate) mod shape_get_session_token_input;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_get_web_identity_token;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_get_web_identity_token_input;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 pub(crate) mod shape_expired_token_exception;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub(crate) mod shape_expired_trade_in_token_exception;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub(crate) mod shape_idp_communication_error_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub(crate) mod shape_idp_rejected_claim_exception;

+#[cfg(feature = "op_decode_authorization_message")]
 pub(crate) mod shape_invalid_authorization_message_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub(crate) mod shape_invalid_identity_token_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_jwt_payload_size_exceeded_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 pub(crate) mod shape_malformed_policy_document_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_outbound_web_identity_federation_disabled_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 pub(crate) mod shape_packed_policy_too_large_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 pub(crate) mod shape_policy_descriptor_type;

+#[cfg(feature = "op_assume_role")]
 pub(crate) mod shape_provided_context;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub(crate) mod shape_region_disabled_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_session_duration_escalation_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub(crate) mod shape_assumed_role_user;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub(crate) mod shape_credentials;

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) mod shape_federated_user;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,9 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub(crate) fn assumed_role_user_correct_errors(
     mut builder: crate::types::builders::AssumedRoleUserBuilder,
 ) -> crate::types::builders::AssumedRoleUserBuilder {
@@ -11,6 +16,15 @@
     builder
 }

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub(crate) fn credentials_correct_errors(
     mut builder: crate::types::builders::CredentialsBuilder,
 ) -> crate::types::builders::CredentialsBuilder {
@@ -29,6 +43,7 @@
     builder
 }

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) fn federated_user_correct_errors(
     mut builder: crate::types::builders::FederatedUserBuilder,
 ) -> crate::types::builders::FederatedUserBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,26 +1,82 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::_credentials::Credentials;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub use crate::types::_assumed_role_user::AssumedRoleUser;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::_policy_descriptor_type::PolicyDescriptorType;

+#[cfg(feature = "op_get_federation_token")]
 pub use crate::types::_federated_user::FederatedUser;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(feature = "op_assume_role")]
 pub use crate::types::_provided_context::ProvidedContext;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 mod _assumed_role_user;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 mod _credentials;

+#[cfg(feature = "op_get_federation_token")]
 mod _federated_user;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 mod _policy_descriptor_type;

+#[cfg(feature = "op_assume_role")]
 mod _provided_context;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 mod _tag;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,12 +1,40 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::_credentials::CredentialsBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub use crate::types::_assumed_role_user::AssumedRoleUserBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::_policy_descriptor_type::PolicyDescriptorTypeBuilder;

+#[cfg(feature = "op_get_federation_token")]
 pub use crate::types::_federated_user::FederatedUserBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(feature = "op_assume_role")]
 pub use crate::types::_provided_context::ProvidedContextBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,50 +1,122 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 pub use crate::types::error::_expired_token_exception::ExpiredTokenException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_packed_policy_too_large_exception::PackedPolicyTooLargeException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::error::_region_disabled_exception::RegionDisabledException;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_idp_rejected_claim_exception::IdpRejectedClaimException;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_invalid_identity_token_exception::InvalidIdentityTokenException;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub use crate::types::error::_idp_communication_error_exception::IdpCommunicationErrorException;

+#[cfg(feature = "op_decode_authorization_message")]
 pub use crate::types::error::_invalid_authorization_message_exception::InvalidAuthorizationMessageException;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub use crate::types::error::_expired_trade_in_token_exception::ExpiredTradeInTokenException;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_jwt_payload_size_exceeded_exception::JwtPayloadSizeExceededException;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_outbound_web_identity_federation_disabled_exception::OutboundWebIdentityFederationDisabledException;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_session_duration_escalation_exception::SessionDurationEscalationException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 mod _expired_token_exception;

+#[cfg(feature = "op_get_delegated_access_token")]
 mod _expired_trade_in_token_exception;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 mod _idp_communication_error_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 mod _idp_rejected_claim_exception;

+#[cfg(feature = "op_decode_authorization_message")]
 mod _invalid_authorization_message_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 mod _invalid_identity_token_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 mod _jwt_payload_size_exceeded_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 mod _malformed_policy_document_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 mod _outbound_web_identity_federation_disabled_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 mod _packed_policy_too_large_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 mod _region_disabled_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 mod _session_duration_escalation_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,24 +1,60 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 pub use crate::types::error::_expired_token_exception::ExpiredTokenExceptionBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentExceptionBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_packed_policy_too_large_exception::PackedPolicyTooLargeExceptionBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::error::_region_disabled_exception::RegionDisabledExceptionBuilder;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_idp_rejected_claim_exception::IdpRejectedClaimExceptionBuilder;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_invalid_identity_token_exception::InvalidIdentityTokenExceptionBuilder;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub use crate::types::error::_idp_communication_error_exception::IdpCommunicationErrorExceptionBuilder;

+#[cfg(feature = "op_decode_authorization_message")]
 pub use crate::types::error::_invalid_authorization_message_exception::InvalidAuthorizationMessageExceptionBuilder;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub use crate::types::error::_expired_trade_in_token_exception::ExpiredTradeInTokenExceptionBuilder;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_jwt_payload_size_exceeded_exception::JwtPayloadSizeExceededExceptionBuilder;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_outbound_web_identity_federation_disabled_exception::OutboundWebIdentityFederationDisabledExceptionBuilder;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_session_duration_escalation_exception::SessionDurationEscalationExceptionBuilder;
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
@@ -89,41 +76,33 @@
 [dependencies.tracing]
 version = "0.1"
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

@@ -155,6 +134,17 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["sigv4a", "rustls", "default-https-client", "rt-tokio"]
+op_assume_role = []
+op_assume_role_with_saml = []
+op_assume_role_with_web_identity = []
+op_assume_root = []
+op_decode_authorization_message = []
+op_get_access_key_info = []
+op_get_caller_identity = []
+op_get_delegated_access_token = []
+op_get_federation_token = []
+op_get_session_token = []
+op_get_web_identity_token = []

 [hints]
 mostly-unused = true
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -90,12 +90,16 @@
     }
 }

+#[cfg(feature = "op_assume_role")]
 mod assume_role;

+#[cfg(feature = "op_assume_role_with_saml")]
 mod assume_role_with_saml;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 mod assume_role_with_web_identity;

+#[cfg(feature = "op_assume_root")]
 mod assume_root;

 /// Operation customization and supporting types.
@@ -125,16 +129,23 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_decode_authorization_message")]
 mod decode_authorization_message;

+#[cfg(feature = "op_get_access_key_info")]
 mod get_access_key_info;

+#[cfg(feature = "op_get_caller_identity")]
 mod get_caller_identity;

+#[cfg(feature = "op_get_delegated_access_token")]
 mod get_delegated_access_token;

+#[cfg(feature = "op_get_federation_token")]
 mod get_federation_token;

+#[cfg(feature = "op_get_session_token")]
 mod get_session_token;

+#[cfg(feature = "op_get_web_identity_token")]
 mod get_web_identity_token;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,30 +3,66 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_assume_root"
+    ))]
     /// <p>The web identity token that was passed is expired or is not valid. Get a new identity token from the identity provider and then retry the request.</p>
     ExpiredTokenException(crate::types::error::ExpiredTokenException),
+    #[cfg(feature = "op_get_delegated_access_token")]
     /// <p>The trade-in token provided in the request has expired and can no longer be exchanged for credentials. Request a new token and retry the operation.</p>
     ExpiredTradeInTokenException(crate::types::error::ExpiredTradeInTokenException),
+    #[cfg(feature = "op_assume_role_with_web_identity")]
     /// <p>The request could not be fulfilled because the identity provider (IDP) that was asked to verify the incoming identity token could not be reached. This is often a transient error caused by network conditions. Retry the request a limited number of times so that you don't exceed the request rate. If the error persists, the identity provider might be down or not responding.</p>
     IdpCommunicationErrorException(crate::types::error::IdpCommunicationErrorException),
+    #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
     /// <p>The identity provider (IdP) reported that authentication failed. This might be because the claim is invalid.</p>
     /// <p>If this error is returned for the <code>AssumeRoleWithWebIdentity</code> operation, it can also mean that the claim has expired or has been explicitly revoked.</p>
     IdpRejectedClaimException(crate::types::error::IdpRejectedClaimException),
+    #[cfg(feature = "op_decode_authorization_message")]
     /// <p>The error returned if the message passed to <code>DecodeAuthorizationMessage</code> was invalid. This can happen if the token contains invalid characters, such as line breaks, or if the message has expired.</p>
     InvalidAuthorizationMessageException(crate::types::error::InvalidAuthorizationMessageException),
+    #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
     /// <p>The web identity token that was passed could not be validated by Amazon Web Services. Get a new identity token from the identity provider and then retry the request.</p>
     InvalidIdentityTokenException(crate::types::error::InvalidIdentityTokenException),
+    #[cfg(feature = "op_get_web_identity_token")]
     /// <p>The requested token payload size exceeds the maximum allowed size. Reduce the number of request tags included in the <code>GetWebIdentityToken</code> API call to reduce the token payload size.</p>
     JwtPayloadSizeExceededException(crate::types::error::JwtPayloadSizeExceededException),
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_get_federation_token"
+    ))]
     /// <p>The request was rejected because the policy document was malformed. The error message describes the specific error.</p>
     MalformedPolicyDocumentException(crate::types::error::MalformedPolicyDocumentException),
+    #[cfg(feature = "op_get_web_identity_token")]
     /// <p>The outbound web identity federation feature is not enabled for this account. To use this feature, you must first enable it through the Amazon Web Services Management Console or API.</p>
     OutboundWebIdentityFederationDisabledException(crate::types::error::OutboundWebIdentityFederationDisabledException),
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_get_delegated_access_token",
+        feature = "op_get_federation_token"
+    ))]
     /// <p>The request was rejected because the total packed size of the session policies and session tags combined was too large. An Amazon Web Services conversion compresses the session policy document, session policy ARNs, and session tags into a packed binary format that has a separate limit. The error message indicates by percentage how close the policies and tags are to the upper size limit. For more information, see <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_session-tags.html">Passing Session Tags in STS</a> in the <i>IAM User Guide</i>.</p>
     /// <p>You could receive this error even though you meet other defined session policy and session tag limits. For more information, see <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html#reference_iam-limits-entity-length">IAM and STS Entity Character Limits</a> in the <i>IAM User Guide</i>.</p>
     PackedPolicyTooLargeException(crate::types::error::PackedPolicyTooLargeException),
+    #[cfg(any(
+        feature = "op_assume_role",
+        feature = "op_assume_role_with_saml",
+        feature = "op_assume_role_with_web_identity",
+        feature = "op_assume_root",
+        feature = "op_get_delegated_access_token",
+        feature = "op_get_federation_token",
+        feature = "op_get_session_token"
+    ))]
     /// <p>STS is not activated in the requested region for the account that is being asked to generate credentials. The account administrator must use the IAM console to activate STS in that region. For more information, see <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp_enable-regions.html#sts-regions-activate-deactivate">Activating and Deactivating STS in an Amazon Web Services Region</a> in the <i>IAM User Guide</i>.</p>
     RegionDisabledException(crate::types::error::RegionDisabledException),
+    #[cfg(feature = "op_get_web_identity_token")]
     /// <p>The requested token duration would extend the session beyond its original expiration time. You cannot use this operation to extend the lifetime of a session beyond what was granted when the session was originally created.</p>
     SessionDurationEscalationException(crate::types::error::SessionDurationEscalationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -43,17 +79,53 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Error::ExpiredTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Error::ExpiredTradeInTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Error::IdpCommunicationErrorException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::IdpRejectedClaimException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_decode_authorization_message")]
             Error::InvalidAuthorizationMessageException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::InvalidIdentityTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::JwtPayloadSizeExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::OutboundWebIdentityFederationDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Error::PackedPolicyTooLargeException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Error::RegionDisabledException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::SessionDurationEscalationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -78,22 +150,59 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Self::ExpiredTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Self::ExpiredTradeInTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Self::IdpCommunicationErrorException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::IdpRejectedClaimException(inner) => inner.meta(),
+            #[cfg(feature = "op_decode_authorization_message")]
             Self::InvalidAuthorizationMessageException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::InvalidIdentityTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::JwtPayloadSizeExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Self::MalformedPolicyDocumentException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::OutboundWebIdentityFederationDisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Self::PackedPolicyTooLargeException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Self::RegionDisabledException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::SessionDurationEscalationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_assume_role")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::assume_role::AssumeRoleError, R>>
     for Error
 where
@@ -111,6 +220,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role")]
 impl From<crate::operation::assume_role::AssumeRoleError> for Error {
     fn from(err: crate::operation::assume_role::AssumeRoleError) -> Self {
         match err {
@@ -130,6 +240,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_saml")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -155,6 +266,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_saml")]
 impl From<crate::operation::assume_role_with_saml::AssumeRoleWithSAMLError> for Error {
     fn from(err: crate::operation::assume_role_with_saml::AssumeRoleWithSAMLError) -> Self {
         match err {
@@ -182,6 +294,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_web_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -207,6 +320,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_role_with_web_identity")]
 impl From<crate::operation::assume_role_with_web_identity::AssumeRoleWithWebIdentityError> for Error {
     fn from(err: crate::operation::assume_role_with_web_identity::AssumeRoleWithWebIdentityError) -> Self {
         match err {
@@ -235,6 +349,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_root")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::assume_root::AssumeRootError, R>>
     for Error
 where
@@ -252,6 +367,7 @@
         }
     }
 }
+#[cfg(feature = "op_assume_root")]
 impl From<crate::operation::assume_root::AssumeRootError> for Error {
     fn from(err: crate::operation::assume_root::AssumeRootError) -> Self {
         match err {
@@ -265,6 +381,7 @@
         }
     }
 }
+#[cfg(feature = "op_decode_authorization_message")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -290,6 +407,7 @@
         }
     }
 }
+#[cfg(feature = "op_decode_authorization_message")]
 impl From<crate::operation::decode_authorization_message::DecodeAuthorizationMessageError> for Error {
     fn from(err: crate::operation::decode_authorization_message::DecodeAuthorizationMessageError) -> Self {
         match err {
@@ -300,6 +418,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_access_key_info")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -325,6 +444,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_access_key_info")]
 impl From<crate::operation::get_access_key_info::GetAccessKeyInfoError> for Error {
     fn from(err: crate::operation::get_access_key_info::GetAccessKeyInfoError) -> Self {
         match err {
@@ -332,6 +452,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_caller_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -357,6 +478,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_caller_identity")]
 impl From<crate::operation::get_caller_identity::GetCallerIdentityError> for Error {
     fn from(err: crate::operation::get_caller_identity::GetCallerIdentityError) -> Self {
         match err {
@@ -364,6 +486,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delegated_access_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -389,6 +512,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delegated_access_token")]
 impl From<crate::operation::get_delegated_access_token::GetDelegatedAccessTokenError> for Error {
     fn from(err: crate::operation::get_delegated_access_token::GetDelegatedAccessTokenError) -> Self {
         match err {
@@ -405,6 +529,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_federation_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -430,6 +555,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_federation_token")]
 impl From<crate::operation::get_federation_token::GetFederationTokenError> for Error {
     fn from(err: crate::operation::get_federation_token::GetFederationTokenError) -> Self {
         match err {
@@ -448,6 +574,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_session_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -473,6 +600,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_session_token")]
 impl From<crate::operation::get_session_token::GetSessionTokenError> for Error {
     fn from(err: crate::operation::get_session_token::GetSessionTokenError) -> Self {
         match err {
@@ -483,6 +611,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_web_identity_token")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -508,6 +637,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_web_identity_token")]
 impl From<crate::operation::get_web_identity_token::GetWebIdentityTokenError> for Error {
     fn from(err: crate::operation::get_web_identity_token::GetWebIdentityTokenError) -> Self {
         match err {
@@ -527,17 +657,53 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Error::ExpiredTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Error::ExpiredTradeInTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Error::IdpCommunicationErrorException(inner) => inner.source(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::IdpRejectedClaimException(inner) => inner.source(),
+            #[cfg(feature = "op_decode_authorization_message")]
             Error::InvalidAuthorizationMessageException(inner) => inner.source(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Error::InvalidIdentityTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::JwtPayloadSizeExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.source(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::OutboundWebIdentityFederationDisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Error::PackedPolicyTooLargeException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Error::RegionDisabledException(inner) => inner.source(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Error::SessionDurationEscalationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -546,17 +712,53 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root"
+            ))]
             Self::ExpiredTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_get_delegated_access_token")]
             Self::ExpiredTradeInTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_assume_role_with_web_identity")]
             Self::IdpCommunicationErrorException(e) => e.request_id(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::IdpRejectedClaimException(e) => e.request_id(),
+            #[cfg(feature = "op_decode_authorization_message")]
             Self::InvalidAuthorizationMessageException(e) => e.request_id(),
+            #[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
             Self::InvalidIdentityTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::JwtPayloadSizeExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_federation_token"
+            ))]
             Self::MalformedPolicyDocumentException(e) => e.request_id(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::OutboundWebIdentityFederationDisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token"
+            ))]
             Self::PackedPolicyTooLargeException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_assume_role",
+                feature = "op_assume_role_with_saml",
+                feature = "op_assume_role_with_web_identity",
+                feature = "op_assume_root",
+                feature = "op_get_delegated_access_token",
+                feature = "op_get_federation_token",
+                feature = "op_get_session_token"
+            ))]
             Self::RegionDisabledException(e) => e.request_id(),
+            #[cfg(feature = "op_get_web_identity_token")]
             Self::SessionDurationEscalationException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,35 +1,46 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_assume_role")]
 /// Types for the `AssumeRole` operation.
 pub mod assume_role;

+#[cfg(feature = "op_assume_role_with_saml")]
 /// Types for the `AssumeRoleWithSAML` operation.
 pub mod assume_role_with_saml;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 /// Types for the `AssumeRoleWithWebIdentity` operation.
 pub mod assume_role_with_web_identity;

+#[cfg(feature = "op_assume_root")]
 /// Types for the `AssumeRoot` operation.
 pub mod assume_root;

+#[cfg(feature = "op_decode_authorization_message")]
 /// Types for the `DecodeAuthorizationMessage` operation.
 pub mod decode_authorization_message;

+#[cfg(feature = "op_get_access_key_info")]
 /// Types for the `GetAccessKeyInfo` operation.
 pub mod get_access_key_info;

+#[cfg(feature = "op_get_caller_identity")]
 /// Types for the `GetCallerIdentity` operation.
 pub mod get_caller_identity;

+#[cfg(feature = "op_get_delegated_access_token")]
 /// Types for the `GetDelegatedAccessToken` operation.
 pub mod get_delegated_access_token;

+#[cfg(feature = "op_get_federation_token")]
 /// Types for the `GetFederationToken` operation.
 pub mod get_federation_token;

+#[cfg(feature = "op_get_session_token")]
 /// Types for the `GetSessionToken` operation.
 pub mod get_session_token;

+#[cfg(feature = "op_get_web_identity_token")]
 /// Types for the `GetWebIdentityToken` operation.
 pub mod get_web_identity_token;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,17 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_decode_authorization_message",
+    feature = "op_get_access_key_info",
+    feature = "op_get_caller_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token",
+    feature = "op_get_web_identity_token"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +30,19 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_decode_authorization_message",
+    feature = "op_get_access_key_info",
+    feature = "op_get_caller_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token",
+    feature = "op_get_web_identity_token"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     _response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -25,82 +51,168 @@
     crate::rest_xml_wrapped_errors::parse_error_metadata(response_body)
 }

+#[cfg(feature = "op_assume_role")]
 pub(crate) mod shape_assume_role;

+#[cfg(feature = "op_assume_role")]
 pub(crate) mod shape_assume_role_input;

+#[cfg(feature = "op_assume_role_with_saml")]
 pub(crate) mod shape_assume_role_with_saml;

+#[cfg(feature = "op_assume_role_with_saml")]
 pub(crate) mod shape_assume_role_with_saml_input;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub(crate) mod shape_assume_role_with_web_identity;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub(crate) mod shape_assume_role_with_web_identity_input;

+#[cfg(feature = "op_assume_root")]
 pub(crate) mod shape_assume_root;

+#[cfg(feature = "op_assume_root")]
 pub(crate) mod shape_assume_root_input;

+#[cfg(feature = "op_decode_authorization_message")]
 pub(crate) mod shape_decode_authorization_message;

+#[cfg(feature = "op_decode_authorization_message")]
 pub(crate) mod shape_decode_authorization_message_input;

+#[cfg(feature = "op_get_access_key_info")]
 pub(crate) mod shape_get_access_key_info;

+#[cfg(feature = "op_get_access_key_info")]
 pub(crate) mod shape_get_access_key_info_input;

+#[cfg(feature = "op_get_caller_identity")]
 pub(crate) mod shape_get_caller_identity;

+#[cfg(feature = "op_get_caller_identity")]
 pub(crate) mod shape_get_caller_identity_input;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub(crate) mod shape_get_delegated_access_token;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub(crate) mod shape_get_delegated_access_token_input;

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) mod shape_get_federation_token;

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) mod shape_get_federation_token_input;

+#[cfg(feature = "op_get_session_token")]
 pub(crate) mod shape_get_session_token;

+#[cfg(feature = "op_get_session_token")]
 pub(crate) mod shape_get_session_token_input;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_get_web_identity_token;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_get_web_identity_token_input;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 pub(crate) mod shape_expired_token_exception;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub(crate) mod shape_expired_trade_in_token_exception;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub(crate) mod shape_idp_communication_error_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub(crate) mod shape_idp_rejected_claim_exception;

+#[cfg(feature = "op_decode_authorization_message")]
 pub(crate) mod shape_invalid_authorization_message_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub(crate) mod shape_invalid_identity_token_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_jwt_payload_size_exceeded_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 pub(crate) mod shape_malformed_policy_document_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_outbound_web_identity_federation_disabled_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 pub(crate) mod shape_packed_policy_too_large_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 pub(crate) mod shape_policy_descriptor_type;

+#[cfg(feature = "op_assume_role")]
 pub(crate) mod shape_provided_context;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub(crate) mod shape_region_disabled_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 pub(crate) mod shape_session_duration_escalation_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub(crate) mod shape_assumed_role_user;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub(crate) mod shape_credentials;

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) mod shape_federated_user;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,9 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub(crate) fn assumed_role_user_correct_errors(
     mut builder: crate::types::builders::AssumedRoleUserBuilder,
 ) -> crate::types::builders::AssumedRoleUserBuilder {
@@ -11,6 +16,15 @@
     builder
 }

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub(crate) fn credentials_correct_errors(
     mut builder: crate::types::builders::CredentialsBuilder,
 ) -> crate::types::builders::CredentialsBuilder {
@@ -29,6 +43,7 @@
     builder
 }

+#[cfg(feature = "op_get_federation_token")]
 pub(crate) fn federated_user_correct_errors(
     mut builder: crate::types::builders::FederatedUserBuilder,
 ) -> crate::types::builders::FederatedUserBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,26 +1,82 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::_credentials::Credentials;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub use crate::types::_assumed_role_user::AssumedRoleUser;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::_policy_descriptor_type::PolicyDescriptorType;

+#[cfg(feature = "op_get_federation_token")]
 pub use crate::types::_federated_user::FederatedUser;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(feature = "op_assume_role")]
 pub use crate::types::_provided_context::ProvidedContext;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 mod _assumed_role_user;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 mod _credentials;

+#[cfg(feature = "op_get_federation_token")]
 mod _federated_user;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 mod _policy_descriptor_type;

+#[cfg(feature = "op_assume_role")]
 mod _provided_context;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 mod _tag;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,12 +1,40 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::_credentials::CredentialsBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity"
+))]
 pub use crate::types::_assumed_role_user::AssumedRoleUserBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::_policy_descriptor_type::PolicyDescriptorTypeBuilder;

+#[cfg(feature = "op_get_federation_token")]
 pub use crate::types::_federated_user::FederatedUserBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_get_federation_token",
+    feature = "op_get_web_identity_token"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(feature = "op_assume_role")]
 pub use crate::types::_provided_context::ProvidedContextBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,50 +1,122 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 pub use crate::types::error::_expired_token_exception::ExpiredTokenException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_packed_policy_too_large_exception::PackedPolicyTooLargeException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::error::_region_disabled_exception::RegionDisabledException;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_idp_rejected_claim_exception::IdpRejectedClaimException;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_invalid_identity_token_exception::InvalidIdentityTokenException;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub use crate::types::error::_idp_communication_error_exception::IdpCommunicationErrorException;

+#[cfg(feature = "op_decode_authorization_message")]
 pub use crate::types::error::_invalid_authorization_message_exception::InvalidAuthorizationMessageException;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub use crate::types::error::_expired_trade_in_token_exception::ExpiredTradeInTokenException;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_jwt_payload_size_exceeded_exception::JwtPayloadSizeExceededException;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_outbound_web_identity_federation_disabled_exception::OutboundWebIdentityFederationDisabledException;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_session_duration_escalation_exception::SessionDurationEscalationException;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 mod _expired_token_exception;

+#[cfg(feature = "op_get_delegated_access_token")]
 mod _expired_trade_in_token_exception;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 mod _idp_communication_error_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 mod _idp_rejected_claim_exception;

+#[cfg(feature = "op_decode_authorization_message")]
 mod _invalid_authorization_message_exception;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 mod _invalid_identity_token_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 mod _jwt_payload_size_exceeded_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 mod _malformed_policy_document_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 mod _outbound_web_identity_federation_disabled_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 mod _packed_policy_too_large_exception;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 mod _region_disabled_exception;

+#[cfg(feature = "op_get_web_identity_token")]
 mod _session_duration_escalation_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,24 +1,60 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root"
+))]
 pub use crate::types::error::_expired_token_exception::ExpiredTokenExceptionBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentExceptionBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token"
+))]
 pub use crate::types::error::_packed_policy_too_large_exception::PackedPolicyTooLargeExceptionBuilder;

+#[cfg(any(
+    feature = "op_assume_role",
+    feature = "op_assume_role_with_saml",
+    feature = "op_assume_role_with_web_identity",
+    feature = "op_assume_root",
+    feature = "op_get_delegated_access_token",
+    feature = "op_get_federation_token",
+    feature = "op_get_session_token"
+))]
 pub use crate::types::error::_region_disabled_exception::RegionDisabledExceptionBuilder;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_idp_rejected_claim_exception::IdpRejectedClaimExceptionBuilder;

+#[cfg(any(feature = "op_assume_role_with_saml", feature = "op_assume_role_with_web_identity"))]
 pub use crate::types::error::_invalid_identity_token_exception::InvalidIdentityTokenExceptionBuilder;

+#[cfg(feature = "op_assume_role_with_web_identity")]
 pub use crate::types::error::_idp_communication_error_exception::IdpCommunicationErrorExceptionBuilder;

+#[cfg(feature = "op_decode_authorization_message")]
 pub use crate::types::error::_invalid_authorization_message_exception::InvalidAuthorizationMessageExceptionBuilder;

+#[cfg(feature = "op_get_delegated_access_token")]
 pub use crate::types::error::_expired_trade_in_token_exception::ExpiredTradeInTokenExceptionBuilder;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_jwt_payload_size_exceeded_exception::JwtPayloadSizeExceededExceptionBuilder;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_outbound_web_identity_federation_disabled_exception::OutboundWebIdentityFederationDisabledExceptionBuilder;

+#[cfg(feature = "op_get_web_identity_token")]
 pub use crate::types::error::_session_duration_escalation_exception::SessionDurationEscalationExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
