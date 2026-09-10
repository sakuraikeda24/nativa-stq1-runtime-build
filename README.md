# Nativa Windows Clean Runtime Builder

This repository builds the Windows x64 clean local runtime used by Nativa Desktop.

## Frozen upstream

- Project: ggml-org/llama.cpp
- Tag: b10516
- Commit: b95502ba9aa0eb73a2f4fc8878d7fbe6a847a0b9
- Platform: Windows x64 CPU

## Build requirements

The clean runtime must be built with:

- OpenMP OFF
- OpenSSL OFF
- BoringSSL OFF
- LibreSSL OFF
- CUDA OFF
- Vulkan OFF
- SYCL OFF
- RPC OFF
- No model bundled

The build must fail if:

- b10516 does not resolve to the frozen commit
- libomp140 or another OpenMP runtime is included
- SSL runtime dependencies are included
- GPU runtime dependencies are included
- a .gguf model file is included

## Target artifact

nativa-llama-b10516-win-x64-clean-v1.zip

A successful GitHub Actions build is not production approval by itself. The runtime must pass standalone Windows functional and performance acceptance before integration into Nativa Desktop.
