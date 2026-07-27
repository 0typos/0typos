<img src="./banner.svg" alt="typo — i let AI Jesus take the wheel" width="100%">

```console
$ whoami
typo — independent security researcher, developer, professional prompt-haver

$ cat ./policy
point AI at a problem. read the diff. keep what survives contact with reality.
```

This is where the AI runs wild.

Everything published here started as something I actually needed — a thing that
broke in the wild, a gap in my own tooling, a problem I got tired of solving by
hand. The machine did most of the typing. I picked the direction, argued with
it, and kept the parts that held up.

It is not slop. It is also not artisanal, hand-carved, small-batch code. It is
the honest middle: fast to build, tested harder than you would expect, and
published because it turned out to be genuinely useful.

---

## ▚ what's parked here

### ▸ [statics](https://github.com/0typos/statics) &nbsp;·&nbsp; `shipping`

Static Linux troubleshooting binaries for the machine you *actually* have to
debug — the one with no package manager, no libc you trust, and no network you
control.

Thirteen architectures. musl and a pinned Zig toolchain, no dynamic
interpreter. Rebuilt every month from the latest upstream sources and published
only when all thirteen build clean and pass under QEMU. Every release ships
SPDX SBOMs and Sigstore attestations.

Two uncached builds get compared byte for byte before anything goes out. AI
wrote a lot of it. AI does not get to skip the reproducibility check.

### ▸ glacialcast &nbsp;·&nbsp; `inbound`

End-to-end-encrypted, low-bandwidth Wayland screen viewer with bounded history.
Rust. Native XDG portal and PipeWire capture with no GStreamer, VA-API H.264
with an in-process software fallback, CENC-encrypted fragmented MP4 served as
MPEG-DASH, and a dependency-free browser viewer on MSE and Clear Key.

Roughly one frame per second, with the cursor tracked separately at up to
thirty. The relay never sees your key and cannot decrypt a thing.

Landing here once I stop finding bugs in it. Current pace suggests a while.

---

## ▚ house rules

- **If it's here, it works.** For me. On my hardware. Under my assumptions.
  Your mileage is a research opportunity.
- **Verification is not negotiable.** Sources pinned by digest, actions pinned
  by SHA, base images pinned by hash. The model is fast and confident, which is
  exactly why the gates exist.
- **Bugs are welcome.** Open an issue. I will point AI Jesus at it and read the
  resulting diff with appropriate suspicion.
- **No warranty, no roadmap, no vibes-based release schedule.** Just cron.

```console
$ ./typo --status
[ OK ]   builds ............ reproducible
[ OK ]   supply chain ...... pinned, digested, attested
[ OK ]   copilot ........... enthusiastic
[WARN]   humans in the loop  1
[ OK ]   status ............ shipping anyway
```
