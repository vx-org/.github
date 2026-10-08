<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/vx-org/.github/main/profile/assets/vx-lockup-dark.svg">
  <img alt="VX" src="https://raw.githubusercontent.com/vx-org/.github/main/profile/assets/vx-lockup-light.svg" width="450">
</picture>
# VX

Run development commands with the runtime versions your project needs.

```console
vx node@22 --version
vx uv run python app.py
vx cargo build --release
```

VX resolves runtimes, prepares their environments, and forwards your arguments.
Project requirements live in `vx.toml`; Providers describe how each runtime is
installed and executed.

[Get started](https://loonghao.github.io/vx/guide/getting-started)
· [Documentation](https://loonghao.github.io/vx/)
· [VX source](https://github.com/loonghao/vx)

## Repositories

| Repository | Responsibility |
| --- | --- |
| [VX](https://github.com/loonghao/vx) | Runtime resolution, installation, cache, and command execution. The main repository is preparing to move to this organization. |
| [mirrors](https://github.com/vx-org/mirrors) | Existing upstream binary archive and synchronization tooling. |
| [vx-rez-adapter](https://github.com/vx-org/vx-rez-adapter) | Boundary between VX and Rez Next repository, solver, and environment semantics. |
| [vx-rez-packages](https://github.com/vx-org/vx-rez-packages) | Definitions and release indexes for platform-specific Rez bundles. |

SDK and bundle integration are under development. Source repositories and
unpublished prototypes do not imply that a runtime or package is available to
install. Use each repository's release assets and validation results to check
availability for your platform.

## Runtime distribution

We are moving toward one distribution repository per runtime. Each repository
must identify its upstream project and license, publish versioned assets for
explicit platforms, and provide checksums and a machine-readable manifest.
The archive must retain upstream provenance and remain compatible with VX's
Provider and cache contracts.

A mirror changes where an artifact is downloaded; it does not change the
upstream project's ownership or support commitments. Upstream binaries keep
their original licenses. Publishing a mirror requires redistribution permission
and the license, notices, and corresponding source obligations of that runtime.

## Contributing

Report runtime resolution and execution issues in
[VX](https://github.com/loonghao/vx/issues). Report an adapter or bundle issue in
the repository that owns it, including the version, platform, command, and
diagnostic output. Never include tokens or other credentials.

---

VX 管理项目所需的开发运行时，让常用命令可以直接执行。
组织内的仓库分别负责运行时管理、二进制分发，以及 Rez Next 适配和包定义。
各平台是否已有可安装产物，请以对应仓库的 Release 和验证结果为准。
