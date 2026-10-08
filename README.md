# lgcorzo/sha256-simd

[![Go Action Status](https://github.com/lgcorzo/sha256-simd/workflows/Go/badge.svg)](https://github.com/lgcorzo/sha256-simd/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/lgcorzo/sha256-simd)](https://goreportcard.com/report/github.com/lgcorzo/sha256-simd)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

Accelerate SHA256 computations in pure Go using AVX-512, Intel SHA Extensions, and ARM64 Cryptography Extensions.
On AVX-512, it provides up to 8x improvement (over 3 GB/s per core).
SHA Extensions give a performance boost of close to 4x over native standard library implementations.

---

## Dark Gravity Factory & Sovereign Support

This repository is actively maintained under **@lgcorzo** as part of the **Sovereign MinIO & Dark Gravity Ecosystem**—a suite of 38 interconnected, high-performance repositories providing enterprise-grade object storage, SIMD-accelerated computing, and cryptographic infrastructure.

### Rationale & Strategic Importance

* **Full Supply-Chain Autonomy:** Eliminates external dependencies and safeguards against upstream license changes, unexpected deprecations, or sudden breaking modifications.
* **Dark Gravity Factory Core Integration:** Powers high-throughput hash verification, payload integrity checks, and data pipeline security for autonomous AI processing and automated agent infrastructure.
* **Compliance & Security:** Sovereign maintenance ensures strict compliance with the **EU AI Act**, **SOC 2 Type II**, **ISO 25059**, and rigorous zero-CVE security SLAs through continuous automated analysis.
* **Ecosystem Interoperability:** Engineered for seamless integration across all 38 repositories in the @lgcorzo ecosystem (MinIO Server, KES, MC, Operator, DirectPV, Console, and SIMD hardware acceleration libraries).

### Automated CI/CD Maintenance Architecture

```
                       ┌──────────────────────────────────────────┐
                       │   Dark Gravity Autonomous AI Factory    │
                       └────────────────────┬─────────────────────┘
                                            │
                          ┌─────────────────┴─────────────────┐
                          ▼                                   ▼
              ┌───────────────────────┐           ┌───────────────────────┐
              │ Sovereign Repositories│           │ Continuous Security & │
              │   (@lgcorzo / 38)     │           │ Automated CI/CD Matrix│
              └───────────┬───────────┘           └───────────┬───────────┘
                          │                                   │
                          └─────────────────┬─────────────────┘
                                            ▼
                       ┌──────────────────────────────────────────┐
                       │  Zero-CVE Compliance & AI Operations    │
                       └──────────────────────────────────────────┘
```

---

## Sovereign Ecosystem (38 Repositories)

| Category | Repository | Description |
| :--- | :--- | :--- |
| **Core Storage Platform** | [`lgcorzo/minio`](https://github.com/lgcorzo/minio) | High-performance, S3-compatible enterprise object storage |
| | [`lgcorzo/mc`](https://github.com/lgcorzo/mc) | MinIO Client for object storage administration |
| | [`lgcorzo/operator`](https://github.com/lgcorzo/operator) | Kubernetes Operator for MinIO clusters |
| | [`lgcorzo/directpv`](https://github.com/lgcorzo/directpv) | CSI driver for direct attached storage |
| | [`lgcorzo/console`](https://github.com/lgcorzo/console) | Graphical management UI for MinIO |
| **Cryptography & Security** | [`lgcorzo/kes`](https://github.com/lgcorzo/kes) | Key Enterprise Server for KMS integration |
| | [`lgcorzo/kms-go`](https://github.com/lgcorzo/kms-go) | Go client for Key Management Service |
| | [`lgcorzo/pkg`](https://github.com/lgcorzo/pkg) | Core security, memory, and utility algorithms |
| | [`lgcorzo/s3-select`](https://github.com/lgcorzo/s3-select) | S3 Select implementation for accelerated queries |
| **Hardware & SIMD Acceleration** | [`lgcorzo/sha256-simd`](https://github.com/lgcorzo/sha256-simd) | SIMD-accelerated SHA256 (AVX-512, ARM64 Crypto) |
| | [`lgcorzo/simdjson-go`](https://github.com/lgcorzo/simdjson-go) | SIMD-accelerated JSON parsing |
| | [`lgcorzo/blake2b-simd`](https://github.com/lgcorzo/blake2b-simd) | SIMD-accelerated BLAKE2b hashing |
| | [`lgcorzo/siphash`](https://github.com/lgcorzo/siphash) | Fast streaming hashing algorithms |
| **SDKs & Client Libraries** | [`lgcorzo/minio-go/v7`](https://github.com/lgcorzo/minio-go) | Official Go SDK for MinIO |
| | [`lgcorzo/madmin-go/v3`](https://github.com/lgcorzo/madmin-go) | Official Go management API for MinIO |
| | [`lgcorzo/minio-dotnet`](https://github.com/lgcorzo/minio-dotnet) | .NET SDK for MinIO |
| | [`lgcorzo/minio-java`](https://github.com/lgcorzo/minio-java) | Java SDK for MinIO |
| | [`lgcorzo/minio-js`](https://github.com/lgcorzo/minio-js) | JavaScript / Node.js SDK for MinIO |
| | [`lgcorzo/minio-python`](https://github.com/lgcorzo/minio-python) | Python SDK for MinIO |
| | [`lgcorzo/minio-go/v6`](https://github.com/lgcorzo/minio-go) | Legacy v6 Go SDK for MinIO |
| | [`lgcorzo/madmin-go/v2`](https://github.com/lgcorzo/madmin-go) | Legacy v2 Go Management SDK |
| | [`lgcorzo/madmin-go`](https://github.com/lgcorzo/madmin-go) | Legacy v1 Go Management SDK |
| **High-Performance IO & Utilities** | [`lgcorzo/dsync`](https://github.com/lgcorzo/dsync) | Distributed sync engine |
| | [`lgcorzo/filepath`](https://github.com/lgcorzo/filepath) | Optimized path manipulation utilities |
| | [`lgcorzo/pkg/v2`](https://github.com/lgcorzo/pkg) | Modern utility primitives v2 |
| | [`lgcorzo/mux`](https://github.com/lgcorzo/mux) | High-performance HTTP routing |
| | [`lgcorzo/cli`](https://github.com/lgcorzo/cli) | CLI helpers for ecosystem tools |
| | [`lgcorzo/color`](https://github.com/lgcorzo/color) | Terminal coloring and formatting |
| | [`lgcorzo/wildcard`](https://github.com/lgcorzo/wildcard) | Fast pattern matching |
| | [`lgcorzo/lsync`](https://github.com/lgcorzo/lsync) | Local synchronization primitives |
| | [`lgcorzo/zip`](https://github.com/lgcorzo/zip) | SIMD-optimized zip archiver |
| | [`lgcorzo/csv`](https://github.com/lgcorzo/csv) | Streaming CSV processing |
| | [`lgcorzo/dnscache`](https://github.com/lgcorzo/dnscache) | DNS caching utilities |
| | [`lgcorzo/xnet`](https://github.com/lgcorzo/xnet) | Extended networking primitives |
| | [`lgcorzo/net`](https://github.com/lgcorzo/net) | High-throughput networking stack |
| | [`lgcorzo/crypto`](https://github.com/lgcorzo/crypto) | Cryptographic helpers and wrappers |
| | [`lgcorzo/targz`](https://github.com/lgcorzo/targz) | Streaming tar.gz processing |
| | [`lgcorzo/par2`](https://github.com/lgcorzo/par2) | Erasure coding and parity utilities |

---

## Introduction

This package is designed as a drop-in acceleration replacement for `crypto/sha256`.
For ARM CPUs with Cryptography Extensions, SHA2 instructions provide massive speedups. For x86 CPUs, AVX-512 and Intel SHA Extensions deliver up to 8x speedup over standard algorithms.

This package uses Go assembly.
The AVX-512 implementation is based on Intel's "multi-buffer crypto library for IPSec", while other x86 implementations follow "Fast SHA-256 Implementations on Intel Architecture Processors" by J. Guilford et al.

## Support for Intel SHA Extensions

Support for Intel SHA Extensions offers a significant performance boost on supported hardware (e.g., Intel Celeron J3455, AMD Ryzen):

```
$ benchcmp avx2.txt sha-ext.txt
benchmark           AVX2 MB/s    SHA Ext MB/s  speedup
BenchmarkHash5M     514.40       1975.17       3.84x
```

Optimized padding and endian conversions further speed up all implementations for small and large inputs.

## Support for AVX-512

AVX-512 results in up to 8x performance improvement over AVX2 (3.0 GHz Xeon Platinum 8124M CPU):

```
$ benchcmp avx2.txt avx512.txt
benchmark           AVX2 MB/s    AVX512 MB/s  speedup
BenchmarkHash5M     448.62       3498.20      7.80x
```

The AVX-512 implementation processes 16 checksums in parallel across ZMM registers. One or more AVX-512 processing servers ([`Avx512Server`](https://github.com/lgcorzo/sha256-simd/blob/master/sha256blockAvx512_amd64.go#L294)) can be instantiated to hash over 3 GB/s per core:

```go
import "github.com/lgcorzo/sha256-simd"

func main() {
	server := sha256.NewAvx512Server()
	h512 := sha256.NewAvx512(server)
	h512.Write(fileBlock)
	digest := h512.Sum([]byte{})
}
```

## Drop-In Replacement

Use `github.com/lgcorzo/sha256-simd` as a standard hash writer:

```go
import "github.com/lgcorzo/sha256-simd"

func main() {
	shaWriter := sha256.New()
	io.Copy(shaWriter, file)
}
```

## Performance

Single-core performance for inputs > 1 MB:

| Processor                         | SIMD    | Speed (MB/s) |
| :-------------------------------- | :------ | -----------: |
| 3.0 GHz Intel Xeon Platinum 8124M | AVX-512 |         3498 |
| 3.7 GHz AMD Ryzen 7 2700X         | SHA Ext |         1979 |
| 1.2 GHz ARM Cortex-A53            | ARM64   |          638 |

## Tooling (asm2plan9s)

To assemble SIMD instructions into Go assembly BYTE sequences, see [`lgcorzo/asm2plan9s`](https://github.com/lgcorzo/asm2plan9s).

## ARM SHA Extensions

ARMv8 Cryptography Extensions accelerate SHA256 computations on ARM platforms:

```
minio@minio-arm:$ benchcmp golang.txt arm64.txt
benchmark                 golang         arm64        speedup
BenchmarkHash8Bytes-4     0.68 MB/s      5.70 MB/s      8.38x
BenchmarkHash1K-4         5.65 MB/s    326.30 MB/s     57.75x
BenchmarkHash8K-4         6.00 MB/s    570.63 MB/s     95.11x
BenchmarkHash1M-4         6.05 MB/s    638.23 MB/s    105.49x
```

## License

Released under the Apache License v2.0. See [LICENSE](LICENSE) for details.
