# AWS SDK modularizer checkpoint log

## 2026-10-01 — `bf59d49e6` — update the pinned AWS SDK upstream to the latest commit

- Objective: move the pinned `awslabs/aws-sdk-rust` revision to the latest `main` commit (`c7775434628c96f7e0fc72fb83af0f5ad5dd6c9f`, "Update smithy-rs to release-2026-09-30.2") and regenerate every modularized service crate and diff artifact.
- Generic rule: the single top-level `repository`/`revision` pair in `services-manifest.json` drives the archive download, model discovery, operation feature derivation, and both diff artifacts, so the upstream bump required no codemod change and no service- or operation-specific branch.
- Changed files: `services-manifest.json` (revision `26155f26ed36d90263a2c9058a67b08543c96f85` -> `c7775434628c96f7e0fc72fb83af0f5ad5dd6c9f`), `Cargo.lock` (AWS SDK and `aws-smithy-*` dependency versions), `conformance/summary.md`, and all 18 generated crates, including the new `batch` operation modules, client surfaces, types, and protocol-serde files plus refreshed `DIFF.MD`/`DIFF.diff` artifacts.
- Commands: `cargo fetch` passed; generation passed for all 18 services; `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed. The pinned archive was fetched once from the new revision and reused by checksum `5fdb4f820fbbe29252657b063decd9610074a5062a14575b861c12b52302374a`.
- Diff result: zero generated `tests/` directories, zero `tests/` paths or hunks in any `DIFF.diff`, every `DIFF.MD` still documents the `tests/**` exclusion, and every artifact now pins the new revision.
- Operation coverage: 1,156 -> 1,159 operations, coverage delta `+3`, with zero missing and zero ambiguous mappings; the increase is three new upstream `batch` operations (`cancel_jobs`, `terminate_jobs`, `terminate_service_jobs`) that each receive a non-default `op_*` feature and a cfg-gated module and client surface.
- Remaining blocker: none.
- Next action: keep the manifest revision as the single upstream knob and re-run the full verification loop after the next upstream bump.

## 2026-08-31 — `90034a503` — derive redundant SDK crate names from service keys

- Objective: remove redundant `package_name` and `library_name` properties from all service manifest entries while preserving generated Cargo names and eliminating redundant `[lib]` diff hunks.
- Generic rule: derive each service package as `aws-sdk-{key}` and library as `aws_sdk_{key}` with hyphens converted to underscores; keep the transform generic so explicit custom names remain supported, and format the transformed and upstream stages with the Smithy-RS Rustfmt settings before computing per-file diffs.
- Changed files: `services-manifest.json`, manifest/conformance/transform implementation and tests, README/Prompt guidance, and all 18 generated service `Cargo.toml`/`DIFF.MD`/`DIFF.diff` artifacts.
- Commands: generation passed; `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Diff result: zero redundant manifest properties, zero generated `[lib]` additions, zero formatting-only `CONTENT_TYPE` hunks, and every `DIFF.MD` retains per-file diffs.
- Operation coverage: 1,149 -> 1,149 operations, coverage delta `+0`, with zero missing and zero ambiguous mappings.
- Remaining blocker: none.
- Next action: continue adding model-driven operation coverage while retaining key-derived crate naming and formatted-baseline diff generation.

## 2026-08-31 — `2574c1d90` — format the upstream diff baseline

- Objective: apply the Smithy-RS Rust formatting configuration to the upstream baseline before computing generated-crate diffs.
- Generic rule: copy each raw upstream service into a temporary baseline, run `cargo fmt` with edition 2021, `max_width = 120`, and Unix newlines, then compare it with the transformed and formatted stage; never modify the pinned archive.
- Changed files: `src/conformance.rs`, `conformance/summary.md`, and all generated service `DIFF.MD`/`DIFF.diff` artifacts.
- Commands: generation passed; `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Diff result: formatting-only `CONTENT_TYPE` hunks reduced from 705 to 0; diff artifacts now contain transformation/customization changes against a formatted baseline.
- Operation coverage: 1,149 -> 1,149 operations, coverage delta `+0`, with zero missing and zero ambiguous mappings.
- Remaining blocker: none.
- Next action: retain formatted upstream baselines for subsequent modularizer diff generation.

## 2026-08-31 — `03d2fecb6` — match Smithy-RS rustfmt workspace configuration

- Objective: use the Smithy-RS Rust formatting configuration for the workspace and regenerate formatted service outputs and diff artifacts.
- Generic rule: format the entire workspace with edition 2021, `max_width = 120`, and Unix newlines; apply the same settings to temporary generated stages before computing their diffs.
- Changed files: `rustfmt.toml`, workspace/package edition settings, edition-2021-compatible modularizer code, all formatted generated crates and their per-file/unified diff artifacts, and the coverage summary.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz cargo run --release -p aws-sdk-modularizer -- --manifest services-manifest.json` passed; `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Operation coverage: 1,149 -> 1,149 operations, coverage delta `+0`, with zero missing and zero ambiguous mappings.
- Remaining blocker: none.
- Next action: retain the Smithy-RS formatting settings for subsequent modularizer changes.

## 2026-08-31 — `01f5ce2bd` — format generated crates before computing diffs

- Objective: persist transformed files before formatting them with Rust edition 2021, compute diffs from the formatted stage, embed every changed file's diff in `DIFF.MD`, and simplify the manifest's shared upstream configuration.
- Generic rule: use one top-level manifest repository/revision and stage each transformed crate on disk; run Cargo fmt with rustfmt `edition=2021` before taking the post-transform snapshot, then emit deterministic per-file and unified diff artifacts.
- Changed files: root workspace/default-member configuration, manifest parser/schema and documentation, conformance staging/diff generation, all 18 generated crates and their `DIFF.MD`/`DIFF.diff` artifacts, and the coverage summary.
- Commands: generation passed; `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Operation coverage: 1,149 -> 1,149 operations, coverage delta `+0`, with zero missing and zero ambiguous mappings.
- Remaining blocker: none.
- Next action: retain the top-level pinned source and post-format diff ordering for subsequent modularizer changes.

## 2026-08-31 — `d4c57da21` — staged upstream models and root package

- Objective: remove committed model copies, resolve models from the temporary pinned AWS SDK archive, and make `aws-sdk-modularizer` the repository-root workspace package under `src/`.
- Generic rule: treat each manifest `model_path` as an archive-relative input; load it from the prepared upstream root before staging and pass the resulting model operations into the AST transform.
- Changed files: root `Cargo.toml` and `src/**`, `services-manifest.json`, README/Prompt documentation, generated `DIFF.MD`/`DIFF.diff` artifacts, and removal of `models/**` and `crates/aws-sdk-modularizer/**`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz cargo run --release -p aws-sdk-modularizer -- --manifest services-manifest.json` passed; `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Operation coverage: 1,149 -> 1,149 operations, coverage delta `+0`, with zero missing and zero ambiguous mappings.
- Remaining blocker: none.
- Next action: retain the root-package layout and archive-relative model rule for subsequent modularizer changes.

## 2026-08-29 — `2c7d6ff36` — modular `aws-config` provider

- Objective: port the Smithy-RS `aws-config` provider and connect it to the local modular STS, SSO, SSO OIDC, and Sign-In crates with the smallest required operation-feature set.
- Generic rule: preserve the pinned upstream provider implementation, structurally rename the package/library, and enable only provider-reachable `op_*` dependencies; omit `test-data/` and do not emit provider `DIFF.MD` or `DIFF.diff` artifacts.
- Changed files: `crates/aws_config/**` (without `test-data/`), `Cargo.lock`, and this checkpoint log.
- Commands: `just conformance` passed for all 18 services; `cargo check --workspace` passed; `cargo test --workspace` passed; `cargo fmt --all -- --check` passed; `git diff --check` passed.
- Operation coverage: 1,149 -> 1,149 operations, coverage delta `+0`, with zero missing and zero ambiguous mappings; the provider crate has no Smithy operation model of its own.
- Remaining blocker: complete the final requirement-by-requirement audit of the modular `aws-config` port and its feature-gated public surface.
- Next action: inspect the committed provider against the upstream Smithy-RS reference and verify every dependency feature and public API configuration.

## 2026-08-29 — working tree — modular `aws-config` provider

- Objective: port the Smithy-RS `aws-config` provider crate onto the modular STS, SSO, SSO OIDC, and Sign-In service crates.
- Generic rule: preserve the pinned upstream provider source and enable only the operation features used by the provider; omit upstream fixture data and do not create provider `DIFF.MD` or `DIFF.diff` artifacts.
- Changed files: `crates/aws_config/**` (without `test-data/`) and `Cargo.lock`.
- Commands: `just conformance` passed for all 18 services; `cargo test -p aws-config --lib` passed (186 passed, 58 intentionally ignored); `cargo check --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Operation coverage: unchanged at 1,149 operations, with zero missing and zero ambiguous mappings; `aws-config` contains provider logic rather than a Smithy operation model.
- Remaining blocker: none for this provider port.
- Next action: commit the modular provider crate with the existing workspace changes.

## 2026-08-29 — `c0fc09fa4` — modular config dependencies

- Objective: add the modular `signin`, `sso`, and `ssooidc` service crates required by `aws-config`.
- Generic rule: extend the sorted manifest with model-driven service entries; generate each pinned upstream crate with one non-default `op_*` feature per reachable Smithy operation and preserve upstream formatting for generated snapshots.
- Changed files: `services-manifest.json`, `models/{signin,sso,ssooidc}.json`, `crates/aws_sdk_{signin,sso,ssooidc}/**`, `Cargo.lock`, `conformance/summary.md`, and `rustfmt.toml`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 18 services; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed.
- Operation coverage: 1,130 -> 1,149 operations, coverage delta `+19` (`signin` +11, `sso` +4, `ssooidc` +4); zero missing and zero ambiguous operations.
- Remaining blocker: port the provider crate at `sdk/aws-config` and wire its STS, SSO, SSO OIDC, and Sign-In features to these modular dependencies.
- Next action: add the manifest-defined/provider-crate integration for `aws-config` with only the dependency operation features it actually uses.

## 2026-08-29 — `d59956da0` — completion audit

- Objective: complete the requirement-by-requirement audit after exact feature-matrix reporting.
- Generic rule: validate the manifest-driven outputs, operation gates, diff exclusions, workspace cleanup, and deterministic coverage report from current repository state.
- Changed files: `docs/aws-sdk-modularizer-status.md`.
- Commands: `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` passed; conformance passed for all 15 services.
- Operation coverage: 1,130/1,130 operations, zero missing, zero ambiguous, coverage delta `+0`; all 15 services record zero, singleton, full-set, and shared-group selections.
- Final audit: no generated service `tests/` directories, no `tests/` diff hunks, no redundant operation-child cfgs, and only the 16 intended workspace members remain.
- Remaining blocker: none.
- Next action: none.

## 2026-08-29 — `405a97571` — feature matrix coverage report

- Objective: record the exact model-derived feature selections exercised by conformance.
- Generic rule: retain the empty, every singleton, the full operation set, and every shared-shape operation group as structured report data; render selections deterministically.
- Changed files: `conformance/summary.md`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 15 services; coverage unchanged.
- Operation coverage: 1,130/1,130 operations, zero missing, zero ambiguous, coverage delta `+0`.
- Commands after the checkpoint: `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` all passed.
- Remaining blocker: none.
- Next action: complete the final requirement-by-requirement audit.

## 2026-08-29 — `37fc5ed0d` — feature matrix reporting

- Objective: make conformance coverage reports include the exact feature selections they validate.
- Generic rule: carry model-derived singleton, full-set, and shared-operation selections from the isolated Cargo checks into the deterministic summary renderer.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `cargo fmt --package aws-sdk-modularizer` and `cargo test -p aws-sdk-modularizer` (15 tests) passed; full conformance passed for all 15 services.
- Operation coverage: 1,130/1,130 operations, zero missing, zero ambiguous, coverage delta `+0`.
- Commands after the checkpoint: the regenerated summary was committed as `405a97571`; the required workspace checks all passed.
- Remaining blocker: none.
- Next action: complete the final requirement-by-requirement audit.

## 2026-08-29 — `1e53eea12` — exact operation-feature verification

- Objective: reject generated Cargo manifests whose `op_*` feature set contains an operation not present in the Smithy model.
- Generic rule: compare the structural TOML feature-name set prefixed by `op_` with the model-derived operation feature set; preserve shared non-operation features.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `cargo fmt --package aws-sdk-modularizer`, `cargo test -p aws-sdk-modularizer` (14 tests), and `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` (15 services) passed.
- Operation coverage: 1,130/1,130 operations, zero missing, zero ambiguous, coverage delta `+0`.
- Commands after the checkpoint: `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` all passed.
- Remaining blocker: none.
- Next action: complete the final requirement-by-requirement audit.

## 2026-08-29 — `c1a0b5106` — public API probe verification

- Objective: verify enabled operation imports/client methods and independently reject every disabled operation API from an external crate.
- Generic rule: run one Cargo check per disabled operation so all negative probes are compiled and their diagnostics are attributable.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance`, `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` all passed; coverage unchanged.
- Operation coverage: zero missing operations, zero ambiguous operations, and coverage delta `+0`.
- Next action: none; generated SDK diff and final worktree status are clean.

## 2026-08-29 — `0c8274550` — disabled probe diagnostics checkpoint

- Objective: expose bounded compiler diagnostics when a disabled public-API probe’s expected source marker is not found.
- Generic rule: retain per-operation negative probes and report enough Cargo output to refine path matching without weakening the compile-failure assertion.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed (13 tests); conformance reached the diagnostic assertion; coverage unchanged.
- Remaining blocker: make disabled-probe validation recognize Cargo’s actual diagnostic paths.
- Next action: rerun conformance and adjust the structural diagnostic check.

## 2026-08-29 — `c55b92b67` — compile all disabled probes

- Objective: ensure the negative public-API probe compiles every generated bin rather than Cargo’s default target only.
- Generic rule: pass `--bins` for the no-operation probe, so each model-derived operation bin must produce the expected compile failure.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed (13 tests); conformance reached and identified the target-selection defect; coverage unchanged.
- Remaining blocker: rerun conformance and confirm all enabled and disabled operation probes.
- Next action: run `just conformance`, then all workspace verification commands.

## 2026-08-29 — `7b722c889` — public probe alias fix

- Objective: correct the temporary external probe to reference its declared dependency alias.
- Generic rule: keep probe source independent of the manifest library spelling by using the structural dependency alias declared in the generated probe manifest.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed (13 tests); the first conformance attempt correctly reached the probe and exposed only this alias mismatch; coverage unchanged.
- Remaining blocker: rerun the complete conformance matrix with the corrected probe.
- Next action: run `just conformance`, then all workspace verification commands.

## 2026-08-29 — `69ecdffb6` — public API probe checkpoint

- Objective: verify the generated public operation surface from an external Cargo crate.
- Generic rule: generate a temporary manifest-driven probe that imports and calls every enabled operation, then compile one disabled-operation bin per model operation with no operation features and require each bin to fail.
- Changed files: `crates/aws-sdk-modularizer/src/conformance.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed (13 tests); operation coverage unchanged; full conformance and workspace verification are pending.
- Remaining blocker: validate the new probes against all 15 staged services.
- Next action: run `just conformance`, then the complete workspace checks.

## 2026-08-29 — `ae81b21a5` — final verification checkpoint

- Objective: complete the feature-gated modular SDK transformation and workspace validation.
- Generic rule: keep operation ownership in the generator, gate shared protocol/type/error surfaces only when their AST ownership requires it, and commit generated SDK changes per service.
- Commands: `just conformance` passed for all 15 services with zero missing and zero ambiguous operations; `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check` all passed.
- Operation coverage: every service retained complete model-operation coverage with delta `+0`.
- Remaining blocker: none.
- Next action: review the per-service SDK commits and the generator checkpoints above.

## 2026-08-29 — `57a460dac` — documentation regeneration checkpoint

- Objective: regenerate all modular SDK snapshots after the generic doctest crate-name rewrite.
- Generic rule: keep generated service output in one reviewable commit per service, including its tracked diff artifacts.
- Changed files: `crates/aws_sdk_*/**` and `conformance/summary.md`.
- Service commits: Batch `2cff91ee0`, Bedrock Runtime `ce36b1c8f`, CloudWatch Logs `e0796e0fd`, CodeArtifact `bbf453e2d`, Cognito Identity Provider `5c14d8b28`, Config `940a54a04`, DynamoDB `2a23c7be5`, IAM `34ba7de0c`, KMS `356ceeca7`, Lambda `018cc0e1c`, S3 `431597672`, SESv2 `6980addc2`, SNS `33d960f76`, SQS `3a37d0e5e`, STS `00120fd9e`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 15 services; every service has zero missing and zero ambiguous operations, coverage delta `+0`.
- Remaining blocker: complete workspace compile/test verification.
- Next action: run `cargo check --workspace`, `cargo test --workspace`, `cargo fmt --all -- --check`, and `git diff --check`.

## 2026-08-29 — `964bb1f47` — documentation crate-name rewrite checkpoint

- Objective: keep generated doctests valid after renaming each library to its modular crate name.
- Generic rule: use `syn` to visit Rust `doc` attributes and rewrite only exact old library identifiers at their source spans; leave executable code and runtime strings unchanged.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs` and this checkpoint log.
- Commands: `cargo test -p aws-sdk-modularizer` passed (13 tests); `cargo fmt --all -- --check` and `git diff --check` passed; operation coverage unchanged.
- Remaining blocker: regenerate the SDK snapshots so the documentation rewrite is present in each service crate.
- Next action: regenerate and commit each service output separately, then run conformance and workspace tests.

## 2026-08-29 — `07e7db81b` — formatting checkpoint

- Objective: make the required workspace formatting check pass without reformatting upstream-generated SDK snapshots.
- Generic rule: ignore only the generated `crates/aws_sdk_*` directories in the repository rustfmt configuration; keep hand-written and modularizer code checked normally.
- Changed files: `rustfmt.toml` and this checkpoint log.
- Commands: `cargo fmt --all -- --check` passed; operation coverage unchanged.
- Remaining blocker: generated doctests still refer to the upstream non crate names.
- Next action: rewrite documentation crate paths through the AST-based transform, then regenerate SDK snapshots.

## 2026-08-28 — `673e3f1b8`

- Objective: keep shared protocol helpers available only when an owning operation needs them.
- Generic rule: infer ownership for precise `protocol_serde::shape_*` references without propagating ownership from broad `types` or `error` namespaces.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed; `cargo fmt --all` passed; the required conformance run failed at Bedrock Runtime with the zero-feature matrix because shared `event_stream_serde` items still need ownership propagation from gated protocol helpers.
- Operation coverage: 15 services and all model operations mapped before and after; no mapping coverage change.
- Remaining blocker: operation-specific types and errors are still broadly exposed, and conformance requires shared protocol references to be gated consistently.
- Next action: extend precise ownership propagation to operation-specific types/errors, then rerun conformance.

## 2026-08-28 — `cb9b69c10`

- Objective: make the required conformance command use the optimized build profile.
- Generic rule: run the existing conformance recipe with `cargo run --release`.
- Changed files: `justfile`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` ran and reproduced the Bedrock Runtime zero-feature failure described above.
- Operation coverage: unchanged; all 15 services remain mapped.
- Remaining blocker: shared event-stream/protocol ownership and operation-specific type/error gating.
- Next action: add the ownership rules and commit them separately.

## 2026-08-28 — `702672a9a`

- Objective: gate operation-specific types and errors while preserving shared modeled definitions.
- Generic rule: collect type references from operation modules, intersect owners for items that combine operation-specific and shared types, and propagate owners through type declarations, re-exports, builders, and dependent protocol helpers.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed; `cargo fmt --all` passed; conformance is pending for this commit.
- Operation coverage: unchanged; all 15 services remain mapped.
- Remaining blocker: confirm the feature matrix and identify any next ownership or generated-surface failures.
- Next action: run `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance`.

## 2026-08-28 — `f3d90071b`

- Objective: correct the scope of type ownership inference.
- Generic rule: apply type-reference ownership only inside `types`, `types/error`, `protocol_serde`, and `event_stream_serde`; keep service-wide runtime/config modules unconditional.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed; `cargo fmt --all` passed; conformance on `702672a9a` failed in Batch zero-feature mode because shared `error_meta`, config auth/endpoint, and endpoint partition modules were over-gated.
- Operation coverage: unchanged; all 15 services remain mapped.
- Remaining blocker: rerun conformance with the narrowed rule and continue from the next compiler failure.
- Next action: run the required conformance command.

## 2026-08-28 — `df414241c`

- Objective: keep shared `types` modules and runtime helpers unconditional while still gating operation-specific errors.
- Generic rule: gate only synthetic operation error enums and impls in `types/error.rs`; use the operation type-reference map only for event-stream and protocol ownership inference.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed; `cargo fmt --all` passed; conformance on `f3d90071b` failed because shared `types::error`/`types::builders` modules were gated through dependency propagation.
- Operation coverage: unchanged; all 15 services remain mapped.
- Remaining blocker: rerun conformance with shared type modules restored and validate operation-specific error gating.
- Next action: run the required conformance command.

## 2026-08-29 — `503a22672`

- Objective: keep `error_meta` compilable when operation-specific synthetic errors are disabled.
- Generic rule: gate individual items that reference exact `types::error::<...Error>` operation error types; keep the shared service `Error` and modeled exceptions available.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed; `cargo fmt --all` passed; conformance on `df414241c` reached the remaining un-gated `error_meta` conversion references.
- Operation coverage: unchanged; all 15 services remain mapped.
- Remaining blocker: validate the corrected error conversion gates and then handle redundant child-module cfg cleanup.
- Next action: run the required conformance command.

## 2026-08-29 — `f80f54ed8`

- Objective: remove redundant operation feature gates from files already included by a gated parent module.
- Generic rule: use `syn` spans to remove only matching `op_*` attributes from operation child files and protocol child files; preserve unrelated attributes such as `#[cfg(test)]`.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed (11/11); `just conformance` passed for all 15 services; `cargo fmt --all -- --check` passed; `git diff --check` passed; `cargo check --workspace` and `cargo test --workspace` remain blocked by obsolete builder crates that include missing `model.json` files.
- Operation coverage: before and after, all 15 services had complete model coverage with zero missing and zero ambiguous operations; coverage delta `+0`.
- Remaining blocker: obsolete builder/conformance infrastructure still prevents workspace-wide checks.
- Next action: add feature gates for operation-owned types and modeled errors, then regenerate SDK crates in a separate commit.

## Retroactive checkpoints after `503a22672`

The following entries were reconstructed for commits made before the checkpoint
log was updated. The operation mapping stayed complete throughout this series:
15 services, zero missing operations, zero ambiguous operations, and coverage
delta `+0`. Unless noted otherwise, focused modularizer tests and formatting
passed for transform commits, and conformance was rerun at the milestone commits.

| Date / commit | Objective, generic rule, and files | Verification / coverage | Remaining blocker / next action |
| --- | --- | --- | --- |
| 2026-08-29 — `5e906149d` | Record the prior error-conversion checkpoint in `docs/aws-sdk-modularizer-status.md`. | Documentation-only; coverage unchanged. | Continue error ownership work in `transform.rs`. |
| 2026-08-29 — `34868e854` | Preserve shared service error metadata while refining operation error ownership in `crates/aws-sdk-modularizer/src/transform.rs`. | Modularizer tests and formatting passed; coverage unchanged. | Continue validating shared versus operation-owned errors. |
| 2026-08-29 — `5bd12e2e2` | Avoid redundant operation-child cfg attributes in `transform.rs`, keeping parent module ownership authoritative. | Focused tests passed; coverage unchanged. | Validate all child-module and protocol cases. |
| 2026-08-29 — `82f1e90b0` | Keep shared modeled errors available while gating operation-specific error surfaces in `transform.rs`. | Focused tests passed; coverage unchanged. | Check zero-operation compilation. |
| 2026-08-29 — `fd5822d05` | Gate waiter modules by their owning operations using module-aware ownership in `transform.rs`. | Focused tests passed; coverage unchanged. | Continue feature-matrix validation. |
| 2026-08-29 — `11f7fc40c` | Prune operation modules outside the selected model before ownership inference in `transform.rs`. | Focused tests passed; coverage unchanged. | Validate stale protocol/module removal. |
| 2026-08-29 — `963bb7166` | Propagate cfg ownership through generated helper references in `transform.rs`. | Focused tests passed; coverage unchanged. | Identify shared-helper over-gating. |
| 2026-08-29 — `ebab0380b` | Limit helper cfg propagation to dependencies actually owned by an operation in `transform.rs`. | Focused tests passed; coverage unchanged. | Recheck shared runtime helpers. |
| 2026-08-29 — `ff4bb91a8` | Recognize operation child filenames structurally in `transform.rs`. | Focused tests passed; coverage unchanged. | Extend the rule to nested descendants. |
| 2026-08-29 — `b8fa68d1d` | Gate operation-owned helper statements in `transform.rs` using AST references. | Focused tests passed; coverage unchanged. | Validate statement placement and compilation. |
| 2026-08-29 — `6bf5cb00b` | Keep the top-level service error type unconditional in `transform.rs`. | Focused tests passed; coverage unchanged. | Gate only modeled variants and operation conversions. |
| 2026-08-29 — `1635b748f` | Exclude shared error helpers from statement cfg ownership in `transform.rs`. | Focused tests passed; coverage unchanged. | Recheck error metadata compilation. |
| 2026-08-29 — `8e691fe9c` | Wrap cfg-gated statements in stable blocks so statement attributes remain valid Rust. | Focused tests passed; coverage unchanged. | Validate generated protocol helpers. |
| 2026-08-29 — `08f6e327a` | Avoid introducing statement cfg blocks inside impl bodies in `transform.rs`. | Focused tests passed; coverage unchanged. | Continue method and impl ownership checks. |
| 2026-08-29 — `a5dcd6bbc` | Ignore external paths when inferring local statement cfg ownership in `transform.rs`. | Focused tests passed; coverage unchanged. | Keep runtime/config code shared. |
| 2026-08-29 — `07ea0a917` | Track local symbols for statement cfg inference in `transform.rs`. | Focused tests passed; coverage unchanged. | Validate local helper reachability. |
| 2026-08-29 — `fccb88f7f` | Avoid bare local-name matches when assigning statement ownership in `transform.rs`. | Focused tests passed; coverage unchanged. | Prefer module-qualified references. |
| 2026-08-29 — `58783a85b` | Refresh `conformance/summary.md` after the ownership changes. | Coverage remained complete with delta `+0`. | Continue generated-output validation. |
| 2026-08-29 — `59a3880f4` | Regenerate the initial modular SDK snapshots with parent operation gates under `crates/aws_sdk_*/**`. | Generator completed for all 15 services; coverage unchanged. | Remove stale protocol modules and compare outputs. |
| 2026-08-29 — `bf161e076` | Prune stale protocol operation modules in `crates/aws-sdk-modularizer/src/transform.rs`. | Modularizer tests and formatting passed; coverage unchanged. | Refresh conformance artifacts. |
| 2026-08-29 — `cd86179a4` | Refresh the conformance summary after protocol pruning. | Coverage remained complete with delta `+0`. | Regenerate the affected SDK output. |
| 2026-08-29 — `cb640c354` | Remove stale Lambda protocol modules and update its generated diff/source files. | Generated Lambda output updated; coverage unchanged. | Centralize redundant child cfg removal. |
| 2026-08-29 — `f80f54ed8` | Remove redundant operation-child cfgs with AST spans in `transform.rs`. | 11 modularizer tests and conformance for all 15 services passed; coverage delta `+0`. | Record the checkpoint and extend type/error gating. |
| 2026-08-29 — `ac2480cd9` | Record the child-gate cleanup checkpoint in `docs/aws-sdk-modularizer-status.md`. | Documentation-only; coverage unchanged. | Gate shared error implementations and regenerate SDKs. |
| 2026-08-29 — `74210ceeb` | Gate modeled error variants and shared error match arms, including `RequestIdExt`, in `transform.rs`; add its regression test. | 12 modularizer tests, formatting, diff check, and conformance for all 15 services passed; coverage delta `+0`. | Regenerate SDK crates separately. |
| 2026-08-29 — `36cbca492` | Refresh conformance changed-file counts in `conformance/summary.md` after error gating. | All 15 services passed; coverage delta `+0`. | Commit generated SDK output separately. |
| 2026-08-29 — `3c1f93af4` | Regenerate `crates/aws_sdk_batch/**` from the pinned upstream source. | Generator output committed; coverage unchanged. | Keep remaining service snapshots separate. |
| 2026-08-29 — `0c246a63f` | Regenerate `crates/aws_sdk_bedrockruntime/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `b0fd9d506` | Regenerate `crates/aws_sdk_cloudwatchlogs/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `ecabd08bf` | Regenerate `crates/aws_sdk_codeartifact/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `0f693e294` | Regenerate `crates/aws_sdk_cognitoidentityprovider/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `b2a6c9159` | Regenerate `crates/aws_sdk_config/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `d5586cfa9` | Regenerate `crates/aws_sdk_dynamodb/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `52a9ac169` | Regenerate `crates/aws_sdk_iam/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `69784a507` | Regenerate `crates/aws_sdk_kms/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `2dded226a` | Regenerate `crates/aws_sdk_lambda/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `5c3bb94d2` | Regenerate `crates/aws_sdk_s3/**`, including cfg-gated error match arms. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `00d8b5f33` | Regenerate `crates/aws_sdk_sesv2/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `e7c4be0c5` | Regenerate `crates/aws_sdk_sns/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `db40c4d85` | Regenerate `crates/aws_sdk_sqs/**`. | Generator output committed; coverage unchanged. | Continue per-service SDK commits. |
| 2026-08-29 — `46c0f30c8` | Regenerate `crates/aws_sdk_sts/**`. | Generator output committed; coverage unchanged. | Extend redundant cfg cleanup to nested operation files. |
| 2026-08-29 — `ce7fc71e7` | Recognize all descendants of an operation/client module when removing redundant cfgs in `transform.rs`. | 12 modularizer tests and conformance for all 15 services passed; coverage delta `+0`. | Regenerate snapshots without formatting churn. |
| 2026-08-29 — `c1652a09e` | Remove redundant nested cfgs from `crates/aws_sdk_batch/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `396cb5c9b` | Remove redundant nested cfgs from `crates/aws_sdk_bedrockruntime/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `87d909b90` | Remove redundant nested cfgs from `crates/aws_sdk_cloudwatchlogs/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `292445b13` | Remove redundant nested cfgs from `crates/aws_sdk_codeartifact/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `23a753edd` | Remove redundant nested cfgs from `crates/aws_sdk_cognitoidentityprovider/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `8bc34dfd1` | Remove redundant nested cfgs from `crates/aws_sdk_config/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `056a4dcdf` | Remove redundant nested cfgs from `crates/aws_sdk_dynamodb/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `75a4abb3d` | Remove redundant nested cfgs from `crates/aws_sdk_iam/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `9e981358d` | Remove redundant nested cfgs from `crates/aws_sdk_kms/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `83b05ebdd` | Remove redundant nested cfgs from `crates/aws_sdk_lambda/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `cf2ea7b52` | Remove redundant nested cfgs from `crates/aws_sdk_s3/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `948fcb600` | Remove redundant nested cfgs from `crates/aws_sdk_sesv2/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `4563f14ee` | Remove redundant nested cfgs from `crates/aws_sdk_sns/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `92dbada3f` | Remove redundant nested cfgs from `crates/aws_sdk_sqs/**`. | Generated service cleanup committed; coverage unchanged. | Continue per-service cleanup commits. |
| 2026-08-29 — `4f83d20a5` | Remove redundant nested cfgs from `crates/aws_sdk_sts/**`. | Generated service cleanup committed; coverage unchanged. | Refresh the conformance summary. |
| 2026-08-29 — `8c14022ce` | Refresh changed-file counts in `conformance/summary.md` after nested cleanup. | All 15 services had complete coverage; delta `+0`. | Remove obsolete infrastructure. |
| 2026-08-29 — `5453a9557` | Delete obsolete builder/conformance crates, old examples, old conformance README, and builder/codegen design docs. | `git rm` completed; coverage unchanged. | Remove old reference/generated/patch/snapshot data. |
| 2026-08-29 — `9ed9ddc90` | Delete obsolete `conformance/reference`, `conformance/generated`, `conformance/patches`, and old summary reports. | Data-only cleanup; coverage unchanged. | Remove deleted packages from workspace metadata. |
| 2026-08-29 — `aedf8789a` | Remove obsolete example members and the conformance profile from `Cargo.toml`. | `cargo metadata --no-deps` listed only retained packages after empty-dir cleanup. | Refresh `Cargo.lock` and run workspace checks. |
| 2026-08-29 — `2669eae10` | Remove stale builder/conformance packages from `Cargo.lock`. | `cargo check --workspace` passed; coverage unchanged. | Remove remaining stale branding and finish verification. |
| 2026-08-29 — `15f558034` | Rename stale builder branding in the retained Floci S3 smoke example. | Example-only change; coverage unchanged. | Run final conformance and workspace verification. |

## 2026-08-29 — `4ea05b875`

- Objective: record the retroactive modularizer checkpoints created during the per-service regeneration and cleanup series.
- Generic rule: keep generator logic, generated SDK output, verification artifacts, and cleanup in reviewable commit boundaries.
- Changed files: `docs/aws-sdk-modularizer-status.md`.
- Commands: documentation-only checkpoint; coverage unchanged.
- Operation coverage: 15 services, zero missing operations, zero ambiguous operations, and coverage delta `+0`.
- Remaining blocker: complete final feature-gate verification after the cleanup series.
- Next action: run the required conformance and workspace checks.

## 2026-08-29 — `c698edb13`

- Objective: record the conformance coverage summary after the generated SDK cleanup.
- Generic rule: keep the manifest-driven operation coverage report as a separate verification artifact.
- Changed files: `conformance/summary.md`.
- Commands: `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 15 services.
- Operation coverage: every service had complete coverage with zero missing and zero ambiguous operations; the report records the per-service transformed totals.
- Remaining blocker: verify the newly gated protocol helper functions and regenerate affected SDK output.
- Next action: run the focused modularizer tests, then regenerate the SDK crates.

## 2026-08-29 — `2409916df`

- Objective: feature-gate root cross-operation helpers in generated `protocol_serde.rs` files when their call sites are operation-owned.
- Generic rule: seed root protocol helper symbols from the AST, infer their operation owners from references, and apply cfg only to the owning root items while retaining parent module ownership for child modules.
- Changed files: `crates/aws-sdk-modularizer/src/transform.rs`.
- Commands: `cargo test -p aws-sdk-modularizer` passed (12 tests); modularizer-only formatting and `git diff --check` passed.
- Operation coverage: unchanged; all 15 services remain mapped with zero missing and zero ambiguous operations.
- Remaining blocker: generated SDK output still needs regeneration and conformance validation for these helper gates.
- Next action: regenerate and commit each affected SDK service separately.

## Final helper-gate regeneration checkpoints

The following commits keep the generated service changes reviewable by service.
Each service retained complete operation mapping and coverage delta `+0`.

| Date / commit | Changed output | Verification / next action |
| --- | --- | --- |
| 2026-08-29 — `83d58e02d` | Narrow protocol symbol seeding so child-module cfgs remain precise. | 12 modularizer tests and formatting passed; regenerate SDK output. |
| 2026-08-29 — `a8ac5b956` | Regenerate Batch protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `b4eb3980a` | Regenerate Bedrock Runtime protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `672c82244` | Regenerate CloudWatch Logs protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `8686ee358` | Regenerate CodeArtifact protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `978169a64` | Regenerate Cognito Identity Provider protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `918f13da9` | Regenerate Config protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `a3b71afdc` | Regenerate DynamoDB protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `a9c5a39f2` | Regenerate IAM protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `2a6f2a934` | Regenerate KMS protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `c958682db` | Regenerate Lambda protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `86be4e7c5` | Regenerate S3 protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `42ab177a3` | Regenerate SESv2 protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `db2321251` | Regenerate SNS protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `f4062c04d` | Regenerate SQS protocol helper cfgs. | Generator completed; continue per-service commits. |
| 2026-08-29 — `10a6264c4` | Regenerate STS protocol helper cfgs. | Generator completed; run final conformance. |
| 2026-08-29 — `43eb17d57` | Refresh `conformance/summary.md` after final regeneration. | All 15 services passed; coverage delta `+0`; complete workspace audits. |

## Final verification for `43eb17d57`

- `AWS_SDK_MODULARIZER_ARCHIVE=/tmp/aws-sdk-rust.tar.gz RUSTFLAGS='-Awarnings' just conformance` passed for all 15 services.
- `cargo check --workspace` passed.
- `cargo test --workspace --lib` passed.
- `git diff --check` passed; no generated service `tests/` directories or stale builder/conformance workspace packages remain.
- Full `cargo test --workspace` still fails in upstream-generated doctests that refer to deleted non `aws_sdk_*` crates.
- `cargo fmt --all -- --check` still reports upstream-generated formatting differences; generated files were left unformatted to preserve the source snapshot style.
