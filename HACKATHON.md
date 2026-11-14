# Swizzle Kernel & Benchmark Hackathon

Welcome to the **Swizzle Community Hackathon**, an open, rolling engineering sprint for systems programmers, Rust developers, GPU kernel hackers, and robotics builders.

Whether you have a 4 GB laptop GPU, an AMD Vulkan card, an Apple Silicon machine, or an H100, you can compete, get your benchmarks onto the live leaderboard, and collaborate directly with the Swizzle core team.

---

## Tracks

### Track 1: Hardware Leaderboard Sweep (10 minutes to enter)
Run `swizzle-rt bench` on your own GPU or CPU and submit your JSON telemetry in [Issue #5](https://github.com/Swizzle-AI/swizzle-runtime/issues/5).

```sh
swizzle-rt pull Qwen/Qwen3-0.6B-GGUF:Q8_0
swizzle-rt bench Qwen3-0.6B-Q8_0.gguf --device cuda --json
```

We are actively collecting verified runs across:
- Consumer NVIDIA GPUs (RTX 3050/3060/4060/4070/4090)
- AMD & Intel GPUs via `--device vulkan`
- x86-64 AVX2 / AVX-512 & ARM64 CPUs

### Track 2: Kernel & Inference Speedups (Rust / CUDA / Vulkan)
Submit a PR that measurably improves throughput, TTFT, memory footprint, or test coverage while preserving **100% bit-exact greedy parity**.
Starter ideas (labeled `good first issue`):
- [#6: Windows PowerShell `install.ps1` & MSVC/CUDA notes](https://github.com/Swizzle-AI/swizzle-runtime/issues/6)
- [#7: Vulkan backend benchmarks & docs](https://github.com/Swizzle-AI/swizzle-runtime/issues/7)
- [#8: OpenAI streaming SSE & `/v1/models` compatibility tests](https://github.com/Swizzle-AI/swizzle-runtime/issues/8)
- [#9: Shell completions (`bash`, `zsh`, `fish`, `powershell`)](https://github.com/Swizzle-AI/swizzle-runtime/issues/9)

### Track 3: Ecosystem & Robotics Demos
Build an open-source demo, agent workflow, or robotics loop powered by `swizzle-rt serve` or the [80.5 Hz Student Robotics Playground](https://swizzle-ten.vercel.app) ([Swizzle Control Plane](https://github.com/Paramveersingh-S/Swizzle)).

---

## Rewards & Collaboration Perks

Early-stage open-source teams grow by building alongside their sharpest contributors. Top participants receive:

1. **Core Collaborator & Swizzle Kernel Fellow Status**: Direct GitHub org collaborator invite (`Swizzle-AI`) and maintainer mentorship on Rust/CUDA kernel PRs.
2. **Co-Authored Engineering Spotlight**: Featured technical writeup on [ML Blueprints Substack](https://mlblueprints.substack.com/p/swizzle-runtime-v010-how-we-reached), `@Swizzler112` on X, and our [Hugging Face Benchmark Dataset](https://huggingface.co/datasets/Scikitlearn10801/swizzle-runtime-benchmarks).
3. **Permanent README & Hall of Fame Credit**: Your GitHub handle and hardware numbers on the README Hardware Leaderboard.
4. **Founding Engineer / Research Collaboration Fast-Track**: Direct 1-on-1 collaboration with the founders on the Swizzle roadmap and priority consideration for paid fellowships or founding team roles as we scale.
5. **Cryptographic Genesis Receipt**: An Ed25519 + BLAKE3 signed contributor receipt generated with `swizzle-rt` and archived in the repository.

---

## How to Submit

1. **Benchmarks**: Post your `swizzle-rt bench --json` output and hardware specs in [Issue #5](https://github.com/Swizzle-AI/swizzle-runtime/issues/5).
2. **Code / Integrations**: Open a PR against `Swizzle-AI/swizzle-runtime` or `Paramveersingh-S/Swizzle` with `[Hackathon]` in the PR title.
