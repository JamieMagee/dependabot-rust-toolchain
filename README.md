# Dependabot Rust Toolchain Example

This is an example repository showcasing how Dependabot can be used to update [Rust toolchains][rust-toolchains] in a project.

## Background

Rust toolchains are defined in a `rust-toolchain.toml` file, which specifies the version of the Rust toolchain to use.
For example:

```toml
[toolchain]
channel = "1.82.0"
```

Dependabot is able to update this file to the latest version of the Rust toolchain, ensuring that your project is always using the most up-to-date and secure version.

## Examples

This repository uses the [`dependabot/example-cli-usage`][example-cli] repository to demonstrate how Dependabot can update the Rust toolchain in a project.

### Versioned Toolchain

[`version/rust-toolchain.toml`](version/rust-toolchain.toml) is an example of a versioned toolchain file that specifies a specific version of the Rust toolchain:

```toml
[toolchain]
channel = "1.82.0"
```

In this case, Dependabot will update the toolchain to the most recent version.
See [commit `617921f34ce3c80b4f9fb55e04e7ff763d881c53`][commit-version] for an example where Dependabot updated the toolchain from `1.82.0` to `1.87.0`.

### Dated Toolchain

[`date/rust-toolchain.toml`](date/rust-toolchain.toml) is an example of a dated toolchain file that specifies a specific date and stability level of the Rust toolchain:

```toml
[toolchain]
channel = "stable-2024-10-17"
```

In this case, Dependabot will update the toolchain to the most recent `stable` version date.
See [commit `e8bb3acbbbfa3c4a6f994df9bcc00ca3a3e5abe5`][commit-date] for an example where Dependabot updated the toolchain from `stable-2024-10-17` to `stable-2025-05-15`.

## Availability

Support is currently in branches:

- [`jamiemagee/rust-toolchain-updater` in `dependabot/dependabot-core`][core]
- [`jamiemagee/rust-toolchain` in `dependabot/cli`][cli]
- [`jamiemagee/rust-toolchain` in `dependabot/smoke-tests`][smoke-tests]

[rust-toolchains]: https://rust-lang.github.io/rustup/concepts/toolchains.html
[core]: https://github.com/dependabot/dependabot-core/tree/jamiemagee/rust-toolchain-updater
[cli]: https://github.com/dependabot/cli/tree/jamiemagee/rust-toolchain
[example-cli]: https://github.com/dependabot/example-cli-usage
[smoke-tests]: https://github.com/dependabot/smoke-tests/tree/jamiemagee/rust-toolchain
[commit-version]: https://github.com/JamieMagee/dependabot-rust-toolchain/commit/617921f34ce3c80b4f9fb55e04e7ff763d881c53
[commit-date]: https://github.com/JamieMagee/dependabot-rust-toolchain/commit/e8bb3acbbbfa3c4a6f994df9bcc00ca3a3e5abe5
