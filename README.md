# typo

I build small, verifiable software for Linux — static binaries that run
anywhere, with build inputs you can audit.

## Projects

**[statics](https://github.com/0typos/statics)** — cross-architecture static
troubleshooting binaries, for when the machine you need to debug has no
package manager and no shared libraries you can trust.

- 13 targets: x86-64, i686, ARM v6/v7 (hard and soft float), AArch64,
  MIPS (BE/LE), PowerPC (32/64, BE/LE), RISC-V 64, and s390x
- Linked against musl with a pinned Zig toolchain — no dynamic interpreter
- Rebuilt monthly from the latest upstream releases, published only when
  every architecture builds and verifies under QEMU
- SPDX SBOMs and Sigstore attestations on every release

## What I care about

- **Reproducible builds** — two uncached builds, compared byte for byte
- **Pinned supply chains** — every source SHA-256'd, every GitHub Action
  SHA-pinned, every base image pinned by digest
- **Verifiable delivery** — checksums, SBOMs, and provenance you can check
  before deploying
